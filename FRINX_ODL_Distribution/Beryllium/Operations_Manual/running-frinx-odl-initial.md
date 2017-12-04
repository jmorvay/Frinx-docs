[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[Operations Manual main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Beryllium/operations_manual.html)
# Starting the FRINX ODL Distribution for the first time (activation)

<!-- TOC START min:1 max:3 link:true update:true -->
- [Running the FRINX ODL Distribution for the first time](#running-the-frinx-odl-distribution-for-the-first-time)
    - [Download and activate the FRINX ODL Distribution](#download-and-activate-the-frinx-odl-distribution)
    - [Start your FRINX ODL Distribution for the first time](#start-your-frinx-odl-distribution-for-the-first-time)
  - [Non-standard setups](#non-standard-setups)
    - [Activating the FRINX ODL Distribution behind a proxy](#activating-the-frinx-odl-distribution-behind-a-proxy)
    - [Activating the FRINX ODL Distribution on a server without Internet access](#activating-the-frinx-odl-distribution-on-a-server-without-internet-access)

<!-- TOC END -->

This guide explains how to run the distribution for the first time. If you have run it previously, please see [this guide](running-frinx-odl-after-activation.md)

***System requirements***  
**RAM:** 4GB minimum; we recommend 8GB.  
**Java:** Releases based on Beryllium and Boron (and subsequent releases) require Java 8.  
**Linux:** Unless stated otherwise, this documentation assumes you are using Linux. Supported distributions are Centos7 and Ubuntu 16.04.  

### Download and activate the FRINX ODL Distribution  

Please click on the following link to download a zip archive of the FRINX ODL Distribution:

*Beryllium*: [distribution-karaf-1.4.10.frinx.zip](https://license.frinx.io/download/distribution-karaf-1.4.10.frinx.zip)  

Older distributions can be downloaded from our [archive](https://frinx.io/archive)
By downloading the file you accept the FRINX software agreement: [EULA](7793505-v7-Frinx-ODL-Distribution-Software-End-User-License-Agreement.pdf)

### Start your FRINX ODL Distribution for the first time

To activate your installation, unzip the file and open the directory. Enter the following commands in a terminal (the token is unique to your user account on frinx.io and cannot be shared with other users. It can be found [here](https://frinx.io/my-licenses-information) (you need to be logged in frinx.io to view your token)

    bin/karaf frinx.createtoken [frinx-license_secret-token]

To stop it, hold down CTRL and type d

## Non-standard setups

### Activating the FRINX ODL Distribution behind a proxy  
Please set up java system properties as described here: <https://docs.oracle.com/javase/6/docs/technotes/guides/net/proxies.html>

This means running karaf with something like this:

    JAVA_OPTS="-Dhttp.proxyHost=10.0.0.100 -Dhttp.proxyPort=8800" bin/karaf frinx.createtoken


### Activating the FRINX ODL Distribution on a server without Internet access  
Let's call the connected computer ONLINE and the one where you want to run karaf OFFLINE.

    OFFLINE# TOKEN="insert your token here"
    OFFLINE# KARAF_HOME="insert path to karaf"
    OFFLINE# echo "token=$TOKEN" &gt; $KARAF_HOME/etc/frinx.license.cfg


Generate fingerprint json to a local file:

    OFFLINE# $KARAF_HOME/bin/karaf frinx.fingerprint > fingerprint.txt


Now, copy fingerprint.txt to the ONLINE machine:

     ONLINE# curl https://license.frinx.io/api/v1/obtain-license -d "@fingerprint.txt"  -H 'Content-Type: application/json' -X PUT > frinx.license.cfg


Copy frinx.license.cfg back to OFFLINE machine, replacing the file in karaf's etc folder. You will be able to start karaf normally:

    OFFLINE# $KARAF_HOME/bin/karaf
