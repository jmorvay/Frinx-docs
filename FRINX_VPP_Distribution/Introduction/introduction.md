[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[VPP operations manual](https://frinxio.github.io/Frinx-docs/FRINX_VPP_Distribution/operations_manual.html)  
# FRINX VPP Distribution: Introduction

FRINX provides an FD.io distribution.  
FD.io is an opensource project that among other things provides the Vector Packet Processor. More information can be found at [FD.io](http://fd.io).  
This page contains the details about the FRINX fd.io distribution.

<!-- TOC START min:1 max:3 link:true update:true -->
- [FRINX VPP Distribution: Introduction](#frinx-vpp-distribution-introduction)
    - [Features](#features)
    - [Operations](#operations)
    - [Jenkins jobs](#jenkins-jobs)

<!-- TOC END -->

### Features

**Project imported from open source:**

*       VPP
    *   No changes

**Internal projects:**

*       VPP-monitoring-agent (magent)

### Operations

**CI/CD**

There is a custom CI/CD pipeline for the FRINX fd.io distribution. It is based on [SBE](../../FRINX_Smart_Build_Engine/Introduction/sbe_intro.md).  
The following diagram shows the relationships between FD.io and FD.FRINX.io:

![fdio](fdio.png)

### Jenkins jobs

The following diagrams list the jenkins jobs imported from opensource FD.io (green marks imported):

![vpp](vpp.png)


