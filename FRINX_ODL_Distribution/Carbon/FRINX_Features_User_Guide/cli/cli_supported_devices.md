[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[FRINX Features User Guide main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Carbon/user_guide.html)
~~~~
{
    "available-cli-device-translations": {
        "available-cli-device-translation": [
            {
                "device-type": "ironware",
                "device-version": "*",
                "units": {
                    "unit": [
                        {
                            "id": "Ironware Interface (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ip?module=frinx-openconfig-if-ip&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14",
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/vlan/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/state",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface",
                                            "/interfaces/interface/state",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Ironware Network Instance (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance-l2&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/state",
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance/connection-points/connection-point/state",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-types?module=frinx-openconfig-network-instance-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-policy-forwarding&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-lsdb&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf-types?module=frinx-openconfig-ospf-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/state",
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance/connection-points/connection-point/state",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-path-groups&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-interfaces&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-forwarding-policies&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-common&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-global&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-l3?module=frinx-openconfig-network-instance-l3&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area-interface&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Ironware cli init (FRINX) translate unit",
                            "models": {}
                        },
                        {
                            "id": "Ironware basic translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:opendaylight:params:xml:ns:yang:ios:essential?module=ios-essential&;revision=2017-05-20",
                                        "implemented-readers": [
                                            "/version"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Baseline translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:opendaylight:params:xml:ns:yang:cli:unit:generic?module=cli-unit-generic&;revision=2017-05-20",
                                        "implemented-rpcs": [
                                            "execute-and-read-until",
                                            "execute",
                                            "execute-and-read"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Ironware CDP (FRINX) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lldp?module=frinx-openconfig-lldp&;revision=2016-05-16",
                                        "implemented-readers": [
                                            "/cdp/interfaces/interface/state",
                                            "/cdp/interfaces/interface",
                                            "/cdp/interfaces/interface/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/cdp?module=frinx-cdp&;revision=2017-10-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lldp/types?module=frinx-openconfig-lldp-types&;revision=2016-05-16"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        }
                    ]
                }
            },
            {
                "device-type": "ios",
                "device-version": "*",
                "units": {
                    "unit": [
                        {
                            "id": "IOS cli init (FRINX) translate unit",
                            "models": {}
                        },
                        {
                            "id": "IOS Network Instance (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance-l2&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/state",
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance/table-connections/table-connection",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/table-connections/table-connection/config",
                                            "/network-instances/network-instance/protocols/protocol/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/state",
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance/connection-points/connection-point/state",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/table-connections",
                                            "/network-instances/network-instance/interfaces/interface/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/interfaces",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/inter-instance-policies",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance/table-connections/table-connection",
                                            "/network-instances/network-instance/table-connections/table-connection/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-types?module=frinx-openconfig-network-instance-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/local-aggregates/aggregate/config",
                                            "/network-instances/network-instance/protocols/protocol/local-aggregates/aggregate"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/local-aggregates/aggregate/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-policy-forwarding&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-lsdb&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf-types?module=frinx-openconfig-ospf-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/state",
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance/table-connections/table-connection",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/table-connections/table-connection/config",
                                            "/network-instances/network-instance/protocols/protocol/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/state",
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance/connection-points/connection-point/state",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/state",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint",
                                            "/network-instances/network-instance/table-connections",
                                            "/network-instances/network-instance/interfaces/interface/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local/config",
                                            "/network-instances/network-instance/connection-points",
                                            "/network-instances/network-instance/interfaces",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/local",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/config",
                                            "/network-instances/network-instance/connection-points/connection-point/config",
                                            "/network-instances/network-instance/inter-instance-policies",
                                            "/network-instances/network-instance/connection-points/connection-point",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance/table-connections/table-connection",
                                            "/network-instances/network-instance/table-connections/table-connection/config",
                                            "/network-instances/network-instance/connection-points/connection-point/endpoints/endpoint/remote"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-path-groups&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-interfaces&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-forwarding-policies&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-common&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-global&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-l3?module=frinx-openconfig-network-instance-l3&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area-interface&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14",
                                        "implemented-writers": [
                                            "/network-instances/network-instance/inter-instance-policies/apply-policy/config",
                                            "/network-instances/network-instance/inter-instance-policies/apply-policy"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Baseline translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:opendaylight:params:xml:ns:yang:cli:unit:generic?module=cli-unit-generic&;revision=2017-05-20",
                                        "implemented-rpcs": [
                                            "execute-and-read-until",
                                            "execute",
                                            "execute-and-read"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS OSPF unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance-l2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-types?module=frinx-openconfig-network-instance-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-policy-forwarding&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-lsdb&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf-types?module=frinx-openconfig-ospf-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-path-groups&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-interfaces&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-forwarding-policies&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-common&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-global&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-l3?module=frinx-openconfig-network-instance-l3&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area-interface&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22",
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/interface-ref",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/interface-ref/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/state",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS Platform unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/platform?module=frinx-openconfig-platform&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/components/component/config",
                                            "/components/component",
                                            "/components/component/state"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/platform-types?module=frinx-openconfig-platform-types&;revision=2017-08-16"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS Local Routing (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/static-routes/static/state",
                                            "/network-instances/network-instance/protocols/protocol/static-routes/static/config",
                                            "/network-instances/network-instance/protocols/protocol/static-routes/static/next-hops/next-hop",
                                            "/network-instances/network-instance/protocols/protocol/static-routes/static",
                                            "/network-instances/network-instance/protocols/protocol/static-routes/static/next-hops/next-hop/config",
                                            "/network-instances/network-instance/protocols/protocol/static-routes/static/next-hops/next-hop/state"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/local-aggregates/aggregate",
                                            "/network-instances/network-instance/protocols/protocol/local-aggregates"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS Routing policy (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14",
                                        "implemented-writers": [
                                            "/routing-policy/defined-sets",
                                            "/routing-policy"
                                        ]
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-policy?module=frinx-openconfig-bgp-policy&;revision=2017-07-30",
                                        "implemented-readers": [
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets/ext-community-set"
                                        ],
                                        "implemented-writers": [
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets",
                                            "/routing-policy/defined-sets/bgp-defined-sets",
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets/ext-community-set/config",
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets/ext-community-set"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS BGP (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/state/prefixes",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/state/prefixes",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/state/prefixes",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/apply-policy/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/apply-policy",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/apply-policy/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/state/prefixes",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/state/prefixes",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/state/prefixes",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/state",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/state/prefixes",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/transport",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS CDP (FRINX) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lldp?module=frinx-openconfig-lldp&;revision=2016-05-16",
                                        "implemented-readers": [
                                            "/cdp/interfaces/interface/state",
                                            "/cdp/interfaces/interface/neighbors/neighbor",
                                            "/cdp/interfaces/interface/config",
                                            "/cdp/interfaces/interface/neighbors/neighbor/state",
                                            "/cdp/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/cdp?module=frinx-cdp&;revision=2017-10-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lldp/types?module=frinx-openconfig-lldp-types&;revision=2016-05-16"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS LLDP (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lldp?module=frinx-openconfig-lldp&;revision=2016-05-16",
                                        "implemented-readers": [
                                            "/lldp/interfaces/interface/state",
                                            "/lldp/interfaces/interface",
                                            "/lldp/interfaces/interface/neighbors/neighbor",
                                            "/lldp/interfaces/interface/neighbors/neighbor/state",
                                            "/lldp/interfaces/interface/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lldp/types?module=frinx-openconfig-lldp-types&;revision=2016-05-16"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS Interface (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ip?module=frinx-openconfig-if-ip&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/vlan/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/vlan/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/state",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface",
                                            "/interfaces/interface/state",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS BGP RIB (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rib/bgp?module=frinx-openconfig-rib-bgp-attributes&;revision=2016-10-17",
                                        "implemented-readers": [
                                            "/bgp-rib/afi-safis/afi-safi",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route/state",
                                            "/bgp-rib/afi-safis/afi-safi/state"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rib/bgp?module=frinx-openconfig-rib-bgp-shared-attributes&;revision=2016-10-17",
                                        "implemented-readers": [
                                            "/bgp-rib/afi-safis/afi-safi",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route/state",
                                            "/bgp-rib/afi-safis/afi-safi/state"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rib/bgp-types?module=frinx-openconfig-rib-bgp-types&;revision=2016-10-17"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rib/bgp?module=frinx-openconfig-rib-bgp-tables&;revision=2016-10-17",
                                        "implemented-readers": [
                                            "/bgp-rib/afi-safis/afi-safi",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route/state",
                                            "/bgp-rib/afi-safis/afi-safi/state"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rib/bgp?module=frinx-openconfig-rib-bgp-table-attributes&;revision=2016-10-17",
                                        "implemented-readers": [
                                            "/bgp-rib/afi-safis/afi-safi",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route/state",
                                            "/bgp-rib/afi-safis/afi-safi/state"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rib/bgp?module=frinx-openconfig-rib-bgp&;revision=2016-10-17",
                                        "implemented-readers": [
                                            "/bgp-rib/afi-safis/afi-safi",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route",
                                            "/bgp-rib/afi-safis/afi-safi/ipv4-unicast/loc-rib/routes/route/state",
                                            "/bgp-rib/afi-safis/afi-safi/state"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    }
                                ]
                            }
                        }
                    ]
                }
            },
            {
                "device-type": "junos",
                "device-version": "*",
                "units": {
                    "unit": [
                        {
                            "id": "Baseline translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:opendaylight:params:xml:ns:yang:cli:unit:generic?module=cli-unit-generic&;revision=2017-05-20",
                                        "implemented-rpcs": [
                                            "execute",
                                            "execute-and-read-until",
                                            "execute-and-read"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Junos cli init (FRINX) translate unit",
                            "models": {}
                        }
                    ]
                }
            },
            {
                "device-type": "vrp",
                "device-version": "*",
                "units": {
                    "unit": [
                        {
                            "id": "VRP BGP (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/apply-policy/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/afi-safis/afi-safi/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "VRP Interface (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ip?module=frinx-openconfig-if-ip&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14",
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/vlan/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/state",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface",
                                            "/interfaces/interface/state",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "VRP Routing policy (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14",
                                        "implemented-writers": [
                                            "/routing-policy/defined-sets",
                                            "/routing-policy"
                                        ]
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-policy?module=frinx-openconfig-bgp-policy&;revision=2017-07-30",
                                        "implemented-readers": [
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets/ext-community-set"
                                        ],
                                        "implemented-writers": [
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets",
                                            "/routing-policy/defined-sets/bgp-defined-sets",
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets/ext-community-set/config",
                                            "/routing-policy/defined-sets/bgp-defined-sets/ext-community-sets/ext-community-set"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Baseline translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:opendaylight:params:xml:ns:yang:cli:unit:generic?module=cli-unit-generic&;revision=2017-05-20",
                                        "implemented-rpcs": [
                                            "execute",
                                            "execute-and-read-until",
                                            "execute-and-read"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "VRP cli init (FRINX) translate unit",
                            "models": {}
                        },
                        {
                            "id": "VRP Network Instance (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance-l2&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/interfaces/interface/config",
                                            "/network-instances/network-instance/interfaces",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-types?module=frinx-openconfig-network-instance-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-policy-forwarding&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-lsdb&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf-types?module=frinx-openconfig-ospf-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/interfaces/interface",
                                            "/network-instances/network-instance/interfaces/interface/config",
                                            "/network-instances/network-instance/interfaces",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-path-groups&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-interfaces&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-forwarding-policies&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-common&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-global&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-l3?module=frinx-openconfig-network-instance-l3&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area-interface&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    }
                                ]
                            }
                        }
                    ]
                }
            },
            {
                "device-type": "ios xr",
                "device-version": "*",
                "units": {
                    "unit": [
                        {
                            "id": "IOS XR ACL unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/acl?module=frinx-openconfig-acl&;revision=2017-05-26",
                                        "implemented-readers": [
                                            "/acl/interfaces/interface/egress-acl-sets/egress-acl-set/config",
                                            "/acl/interfaces/interface/ingress-acl-sets/ingress-acl-set/config",
                                            "/acl/interfaces/interface/config",
                                            "/acl/interfaces/interface/ingress-acl-sets/ingress-acl-set",
                                            "/acl/interfaces/interface",
                                            "/acl/interfaces/interface/egress-acl-sets/egress-acl-set",
                                            "/acl/acl-sets/acl-set"
                                        ],
                                        "implemented-writers": [
                                            "/acl/interfaces/interface",
                                            "/acl/interfaces/interface/config",
                                            "/acl/interfaces/interface/ingress-acl-sets/ingress-acl-set",
                                            "/acl/interfaces/interface/ingress-acl-sets/ingress-acl-set/config",
                                            "/acl/interfaces/interface/egress-acl-sets/egress-acl-set",
                                            "/acl",
                                            "/acl/interfaces/interface/egress-acl-sets/egress-acl-set/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS XR BGP (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/afi-safis/afi-safi/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/bgp/global/config",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors",
                                            "/network-instances/network-instance/protocols/protocol/bgp/neighbors/neighbor/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS cli init (FRINX) translate unit",
                            "models": {}
                        },
                        {
                            "id": "IOS XR SNMP unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/event-types?module=frinx-event-types&;revision=2017-10-24"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/snmp?module=frinx-snmp&;revision=2017-10-24",
                                        "implemented-readers": [
                                            "/snmp/interfaces/interface/config/enabled-trap-for-event",
                                            "/snmp/interfaces/interface/config",
                                            "/snmp/interfaces",
                                            "/snmp/interfaces/interface"
                                        ],
                                        "implemented-writers": [
                                            "/snmp/interfaces/interface",
                                            "/snmp/interfaces/interface/config/enabled-trap-for-event",
                                            "/snmp/interfaces/interface/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS XR Routing policy (OpenConfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "io.frinx.cli.iosxr.logging.LoggingUnit@1e857a41",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/event-types?module=frinx-event-types&;revision=2017-10-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/logging?module=frinx-logging&;revision=2017-10-24",
                                        "implemented-readers": [
                                            "/logging/interfaces/interface/config",
                                            "/logging/interfaces",
                                            "/logging/interfaces/interface/config/enabled-logging-for-event",
                                            "/logging/interfaces/interface"
                                        ],
                                        "implemented-writers": [
                                            "/logging/interfaces/interface",
                                            "/logging/interfaces/interface/config",
                                            "/logging/interfaces/interface/config/enabled-logging-for-event"
                                        ]
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "Baseline translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:opendaylight:params:xml:ns:yang:cli:unit:generic?module=cli-unit-generic&;revision=2017-05-20",
                                        "implemented-rpcs": [
                                            "execute",
                                            "execute-and-read-until",
                                            "execute-and-read"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS XR Network Instance (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance-l2&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/state",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance/state"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-types?module=frinx-openconfig-network-instance-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-policy-forwarding&;revision=2017-06-21",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-lsdb&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf-types?module=frinx-openconfig-ospf-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/state",
                                            "/network-instances/network-instance/config",
                                            "/network-instances/network-instance/state"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance",
                                            "/network-instances/network-instance/protocols/protocol",
                                            "/network-instances/network-instance/protocols/protocol/config",
                                            "/network-instances/network-instance/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-path-groups&;revision=2017-06-21",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-interfaces&;revision=2017-06-21",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-forwarding-policies&;revision=2017-06-21",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface/config",
                                            "/network-instances/network-instance/policy-forwarding/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-common&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-global&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance/pf-interfaces-extension/cisco?module=frinx-cisco-pf-interfaces-extension&;revision=2017-11-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-l3?module=frinx-openconfig-network-instance-l3&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area-interface&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS XR MPLS (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel",
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface/config",
                                            "/network-instances/network-instance/mpls/lsps",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes",
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes/config",
                                            "/network-instances/network-instance/mpls"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance-l2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-types?module=frinx-openconfig-network-instance-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-policy-forwarding&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls/cisco?module=frinx-cisco-mpls-te-extension&;revision=2017-10-24",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/cisco-mpls-te-extension/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/cisco-mpls-te-extension/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-lsdb&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf-types?module=frinx-openconfig-ospf-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls/extension?module=frinx-mpls-rsvp-extension&;revision=2017-10-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-path-groups&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel",
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface/config",
                                            "/network-instances/network-instance/mpls/lsps",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes",
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes/config",
                                            "/network-instances/network-instance/mpls"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-interfaces&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-forwarding-policies&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-common&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-global&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/mpls/signaling-protocols/rsvp-te/interface-attributes/interface/config",
                                            "/network-instances/network-instance/mpls/signaling-protocols/rsvp-te/interface-attributes/interface"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/mpls/signaling-protocols/rsvp-te/interface-attributes/interface/subscription/config",
                                            "/network-instances/network-instance/mpls/signaling-protocols/rsvp-te",
                                            "/network-instances/network-instance/mpls/signaling-protocols/rsvp-te/interface-attributes/interface",
                                            "/network-instances/network-instance/mpls/signaling-protocols/rsvp-te/interface-attributes/interface/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-l3?module=frinx-openconfig-network-instance-l3&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area-interface&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel",
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface/config",
                                            "/network-instances/network-instance/mpls/lsps",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes",
                                            "/network-instances/network-instance/mpls/te-interface-attributes/interface",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/config",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path",
                                            "/network-instances/network-instance/mpls/lsps/constrained-path/tunnels/tunnel/p2p-tunnel-attributes/config",
                                            "/network-instances/network-instance/mpls"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS XR Interface (Openconfig) translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/cisco?module=frinx-cisco-if-extension&;revision=2017-10-24",
                                        "implemented-readers": [
                                            "/interfaces/interface/statistics/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/statistics/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/damping?module=frinx-damping&;revision=2017-10-24",
                                        "implemented-readers": [
                                            "/interfaces/interface/damping/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/damping/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/aggregation/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/aggregation",
                                            "/interfaces/interface/aggregation/config"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ip?module=frinx-openconfig-if-ip&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv6/addresses/address/config",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address",
                                            "/interfaces/interface/subinterfaces/subinterface/ipv4/addresses/address/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lacp-lag-member?module=frinx-lacp-lag-member&;revision=2017-11-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/bfd?module=frinx-bfd&;revision=2017-10-24",
                                        "implemented-readers": [
                                            "/interfaces/interface/aggregation/bfd/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/aggregation/bfd/config",
                                            "/interfaces/interface/aggregation/bfd"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/lacp?module=frinx-openconfig-lacp&;revision=2017-05-05"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/ethernet/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/ethernet",
                                            "/interfaces/interface/ethernet/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14",
                                        "implemented-readers": [
                                            "/interfaces/interface/subinterfaces/subinterface/vlan/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/subinterfaces/subinterface/vlan/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/interfaces/interface/hold-time/config",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ],
                                        "implemented-writers": [
                                            "/interfaces/interface/hold-time/config",
                                            "/interfaces/interface",
                                            "/interfaces/interface/config",
                                            "/interfaces/interface/subinterfaces/subinterface",
                                            "/interfaces/interface/subinterfaces/subinterface/config"
                                        ]
                                    }
                                ]
                            }
                        },
                        {
                            "id": "IOS XR OSPF unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan-types?module=frinx-openconfig-vlan-types&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-igp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance-l2&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-types?module=frinx-openconfig-network-instance-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/local-routing?module=frinx-openconfig-local-routing&;revision=2017-05-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-policy-forwarding&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-yang-types?module=ietf-yang-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-interfaces?module=ietf-interfaces&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/header-fields?module=frinx-openconfig-packet-match&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp-types?module=frinx-openconfig-bgp-types&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-lsdb&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/packet-match-types?module=frinx-openconfig-packet-match-types&;revision=2017-05-26"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf-types?module=frinx-openconfig-ospf-types&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:TBD:params:xml:ns:yang:network-topology?module=network-topology&;revision=2013-10-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-types?module=frinx-openconfig-types&;revision=2017-01-13"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance?module=frinx-openconfig-network-instance&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:ietf-inet-types?module=ietf-inet-types&;revision=2013-07-15"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/aggregate?module=frinx-openconfig-if-aggregate&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospf/cisco?module=frinx-cisco-ospf-extension&;revision=2017-11-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-multiprotocol&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-path-groups&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/openconfig-ext?module=frinx-openconfig-extensions&;revision=2017-01-29"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-interfaces&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-global&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-forwarding?module=frinx-openconfig-pf-forwarding-policies&;revision=2017-06-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces/ethernet?module=frinx-openconfig-if-ethernet&;revision=2016-12-22"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/yang?module=frinx-openconfig-yang-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-common&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-global&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/rsvp?module=frinx-openconfig-mpls-rsvp&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-common-structure&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/network-instance-l3?module=frinx-openconfig-network-instance-l3&;revision=2017-02-28"
                                    },
                                    {
                                        "id": "urn:opendaylight:yang:extension:yang-ext?module=yang-ext&;revision=2013-07-09"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area-interface&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/uniconfig-topology?module=frinx-uniconfig-topology&;revision=2017-11-21"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls?module=frinx-openconfig-mpls-te&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/vlan?module=frinx-openconfig-vlan&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/interfaces?module=frinx-openconfig-interfaces&;revision=2016-12-22",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/interface-ref/config"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/interface-ref",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/interface-ref/config"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "urn:ietf:params:xml:ns:yang:iana-if-type?module=iana-if-type&;revision=2014-05-08"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/ospfv2?module=frinx-openconfig-ospfv2-area&;revision=2017-02-28",
                                        "implemented-readers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area"
                                        ],
                                        "implemented-writers": [
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/global/timers/max-metric/config",
                                            "/network-instances/network-instance/protocols/protocol/ospfv2/areas/area/interfaces/interface"
                                        ]
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/types/inet?module=frinx-openconfig-inet-types&;revision=2017-04-03"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/routing-policy?module=frinx-openconfig-routing-policy&;revision=2017-07-14"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/mpls-types?module=frinx-openconfig-mpls-types&;revision=2017-08-24"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-peer-group&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/bgp?module=frinx-openconfig-bgp-neighbor&;revision=2017-02-02"
                                    },
                                    {
                                        "id": "http://frinx.openconfig.net/yang/policy-types?module=frinx-openconfig-policy-types&;revision=2016-05-12"
                                    }
                                ]
                            }
                        }
                    ]
                }
            },
            {
                "device-type": "*",
                "device-version": "*",
                "units": {
                    "unit": [
                        {
                            "id": "Baseline translate unit",
                            "models": {
                                "model": [
                                    {
                                        "id": "urn:opendaylight:params:xml:ns:yang:cli:unit:generic?module=cli-unit-generic&;revision=2017-05-20",
                                        "implemented-rpcs": [
                                            "execute-and-read-until",
                                            "execute",
                                            "execute-and-read"
                                        ]
                                    }
                                ]
                            }
                        }
                    ]
                }
            }
        ]
    }
}
~~~~
