[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[FRINX Features User Guide main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/user_guide.html)
# L2VPN Service Module User Guide

<!-- TOC START min:1 max:3 link:true update:true -->
- [L2VPN Service Module User Guide](#l2vpn-service-module-user-guide)
  - [Overview](#overview)
  - [A bit about L2VPN](#a-bit-about-l2vpn)
    - [Problem definition and L2VPN](#problem-definition-and-l2vpn)
    - [Terminology](#terminology)
    - [L2VPN types](#l2vpn-types)
  - [L2VPN Provider](#l2vpn-provider)
    - [Use Case Specification](#use-case-specification)
    - [Architecture](#architecture)
    - [Network Element Plugin](#network-element-plugin)
    - [Limitations](#limitations)
    - [User-facing features](#user-facing-features)

<!-- TOC END -->

## Overview

The goal of this project is to automate provisioning of Layer 2 Virtual Private Networks (L2VPN) on Service Provider (SP) routers. This is done by using the Frinx ODL controller which configures routers based on intent of the L2VPN service. The Frinx ODL controller translates the L2VPN service abstraction to network element configuration. ![L2VPN Service](l2vpn_service.png)

## A bit about L2VPN

### Problem definition and L2VPN

A company needs to reconnect multiple sites with each other via an SP which provides L2 services to the company. The company's sites needs to see each other as directly connected on L3. L2VPN offers a solution for those requirements.

The company has two different sites and they are both connected to the Service Provider using an L2 connection. They need to interconnect two of their sites. ![Two company's sites connected to SP](problem.png)

In this case L2VPN provides site-to-site connectivity and the SP network behaves as a wire between the company’s sites. The company’s routes are exchanged via the SP network. ![Solution with L2VPN between sites.](problem_solution.png)

### Terminology

These terms are usually used in the L2VPN domain:

*   **Customer Edge (CE)** device – router at customer site connected to SP
*   **Provider Edge (PE)** device – router at the edge of the SP network which provides connectivity for CE
*   **Provider (P)** device – core router on the SP network providing connectivity among PE routers

![Terminology in picture](terminology.png)

### L2VPN types

There are two main types of L2VPN:

*   point-to-point
*   point-to-multipoint

These types have many implementations. The Frinx ODL distribution supports Virtual Private Wire Service (VPWS) implementation.

#### VPWS

VPWS (Virtual Private Wire Service) is the simplest form for enabling Ethernet services over MPLS. It is also known as ETHoMPLS (Ethernet over MPLS), or VLL (Virtual Leased Line). VPWS is point-to-point L2VPN which usually uses MPLS in core networks for signaling and creates pseudo-wires on PE routers for separation of L2 connections. L2 connections are identified by interface or VLAN. The picture below shows an MPLS core network with pseudo-wires on PEs for each VPN which are identified by VLAN.

![VPWS example](vpws_topology.png)

## L2VPN Provider

L2VPN Provider is an implementation which automatically provisions L2VPN on PE routers based on intended L2VPN service. It exposes a domain specific API for L2VPN manipulation and declarative configuration “what vs how”. L2VPN Provider supports network wide transactions which are transactions on top of multiple devices. Rollback of a network wide transaction means rollback of configuration on each device which was a part of the conifiguration. The rollback of a network wide transaction is done automatically if there is failed configuration on at least one device.

### Use Case Specification

L2VPN Provider can be used on a network where:

*   VPWS L2VPN is needed
*   VLAN is used for pseudo-wire selection
*   MPLS encapsulation is used in SP core

![Use case example](use-case.png)

L2VPN Provider works only with devices which have these capabilities:
<table>
  <thead>
    <tr>
      <th>
        Name
      </th>
      <th>
        Revision
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        Cisco-IOS-XR-l2-eth-infra-cfg
      </td>
      <td>
        2015-11-09
      </td>
    </tr>
    <tr>
      <td>
        Cisco-IOS-XR-ifmgr-cfg
      </td>
      <td>
        2015-07-30
      </td>
    </tr>
    <tr>
      <td>
        Cisco-IOS-XR-l2vpn-cfg
      </td>
      <td>
        2015-11-09
      </td>
    </tr>
    <tr>
      <td>
        rollback-on-error
      </td>
      <td>
      </td>
    </tr>
  </tbody>
</table>

The capabilities are sent from XR to ODL automatically during device connection via NETCONF.
You can see the NETCONF capabilities under each node by calling: 
GET http://{{odl_ip}}:8181/restconf/operational/network-topology:network-topology/topology/topology-netconf

A list of PE nodes can be obtained from: 
GET http://{{odl_ip}}:8181/restconf/operational/network-topology:network-topology/topology/l2vpn-provider-edge-topology

### Architecture

L2VPN Provider is composed of multiple components. The high level architecture is shown in the picture below.

![Architecture](architecture.png)

An external application modifies *ietf-l2vpn* in CONF DS. L2VPN can be configured on nodes which are read from *l2vpn-provider-edge-topology*. When all changes are done, the external application calls RPC *commit-l2vpn*. The RPC reads *ietf-l2vpn* from CONF DS (the intended state) and from OPER DS (the actual state). Diff is created based on intended and actual state. This diff is configured inside network wide transaction on the necessary PE routers by using particular Network Element Plugins. If configuration of routers is successful then a new *ietf-l2vpn* is stored to OPER DS and RPC output is returned with status "complete". In case configuration on one of the devices fails, the rollback of the network wide transaction starts and if the rollback is successful then RPC output has status "commit-failed-rollback-complete", otherwise the status is "inconsistent". The architecture can be extended very easily because Network Element Plugin needs to implement only NEP SPI, rollback, and network element registration. IOS NEP from the picture is not yet implemented.

As was mentioned, NEP registers network elements to L2VPN Provider. L2VPN Provider stores network elements as nodes to abstract topology *l2vpn-provider-edge-topology* and this topology is a source of nodes which can be used for L2VPN configuration.

#### API description

The API is described using YANG modules. An external application can consume the API via RESTCONF, NETCONF, or JAVA. The L2VPN service module provides domain specific abstraction where the abstraction describes attributes of VPNs and sites instead of configuration of network elements. The FRINX ODL Distribution translates the abstraction to network element configuration.

##### [ietf-l2vpn@2017-08-02.yang](ietf-l2vpn@2017-08-02_new.yang)

Original YANG is from [RFC draft - YANG Data Model for MPLS-based L2VPN][9]. This YANG module is modified due to compatibility with OpenDaylight and is extended with L2VPN Provider elements - see the modified YANG module [ietf-l2vpn@2017-08-02.yang](ietf-l2vpn@2017-08-02_new.yang)

The YANG module contains 2 root statements and one RPC:

*   **container l2vpn** – represents intended state stored in CONF DS and actual state stored in OPER DS
*   **container l2vpn-state** – not used in current implementation
*   **rpc commit-l2vpn** – configures intent of L2VPN service. The output of RPC is the result of service configuration.

The following YANGs are modified due to compatibility with OpenDaylight: [ietf-mpls](ietf-mpls@2017-08-02_new.yang)  
[ietf-routing](ietf-routing@2017-08-02_new.yang)   [ietf-routing-types](ietf-routing-types@2017-08-02_new.yang)  

### Network Element Plugin

Network Element Plugin (NEP) is a unit which implements SPI from the L2VPN Provider. This NEP is device API specific and is responsible for:

*   announcement of discovered device (PE) to the L2VPN Provider
*   translation between SPI Data Transfer Objects (DTO) and device configuration
*   rollback of configuration on a device

#### IOS-XRv Network Element Plugin

This plugin configures L2VPN on IOS-XRv using NETCONF. It listens on topology-netconf and announces PE capable devices to the L2VPN Provider. Rollback on a device is done automatically using the "Rollback-on-Error" capability.

![IOS-XRv NEP][10]

IOS-XRv NEP listens on nodes in *topology-netconf*. When a new IOS-XRv device is connected to Frinx ODL it appears as a new node in *topology-netconf* and IOS-XRv registers that node as PE to L2VPN Provider. If L2VPN Provider calls SPI in order to configure PEs via the IOS-XRv NEP, NETCONF is used for device configuration.

Here is an example of L2VPN configuration on IOS-XRv (parameters encapsulated in ** are specific for VPN or site):

<pre>interface **GigabitEthernet0/0/0/0** l2transport
 no shutdown
!

interface **GigabitEthernet0/0/0/0.3001** l2transport
 encapsulation dot1q **3001**
 rewrite ingress tag pop 1 symmetric
 no shutdown
!

l2vpn
 pw-class **PW1**
  encapsulation mpls
   control-word
  !
 !
 xconnect group **frinx**
  p2p **ce1**
   interface **GigabitEthernet0/0/0/0.3001**
   neighbor ipv4 **172.16.2.2** pw-id **999**
    pw-class **PW1**
   !
  !
 !
!
</pre>

#### Mock Network Element Plugin

The purpose of this plugin is to mock functionality of the Network Element Plugin. It is mainly use for testing when you do not need to connect real devices. ![Mock NEP][11]

The Mock NEP listens on nodes from *mock-pe-topology*. When a node is created, the NEP registers this node as a PE node to the L2VPN Provider. When the L2VPN Provider calls the SPI which Mocks NEP implements, intead of configuration of real devices, the SPI DTOs are logged.

### Limitations

Implementation of L2VPN provider does not support all statements in ietf-l2vpn@2017-08-02.yang. All supported elements are listen in the postman collection. L2VPN Provider does not support reconciliation, therefore only L2VPNs created via L2VPN Provider are visible through the API.

Other limitations:

*   only MPLS encapsulation is supported
*   only VLAN can be used between CE and PE for pseudo-wire selection
*   pre-configured MPLS among PEs must exist

### User-facing features

#### frinx-l2vpn-iosxrv

**Karaf installation:**

    feature:install frinx-l2vpn-iosxrv


**Description:**  
Installs L2VPN Provider with IOS-XRv NEP and NETCONF connector. This feature is NEP for IOS-XRv devices.

#### frinx-l2vpn-testing

**Karaf installation:**

    feature:install frinx-l2vpn-testing


**Description:**  
Installs L2VPN Provider with Mock NEP and RESTCONF. This feature can be used for testing and demonstration purposes where real PE devices are not available.

*The postman collection for the L2VPN service module can be accessed [here][1]*

| Feature Guide         |             |                                                                                                     |
|-----------------------|-------------|-----------------------------------------------------------------------------------------------------|
| Feature introduced in | FRINX 2.3.1 | VPN service module implementation with support for L2VPN and IOS XR (Version 6.1.2) NEP via NETCONF |  


 [1]: L2VPN_IOS-XRv_public.postman_collection.json
 [9]: https://tools.ietf.org/html/draft-ietf-bess-l2vpn-yang-05
 [10]: nep_ios-xrv.png "IOS-XRv NEP"
 [11]: nep_mock.png "Mock NEP"
