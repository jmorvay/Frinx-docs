[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[SBE operations manual](https://frinxio.github.io/Frinx-docs/FRINX_Smart_Build_Engine/operations_manual.html) 
# SBE: Proxy server configuration

<!-- TOC START min:1 max:3 link:true update:true -->
- [SBE: Proxy server configuration](#sbe-proxy-server-configuration)
  - [Proxy settings](#proxy-settings)
  - [Proxy control](#proxy-control)

<!-- TOC END -->

This part describes how to set up the SBE proxy server if you provide more SBE instances on more hosts. SBE proxy server is a reverse proxy server provided by NGINX.

**Figure 1: Multi host provision**  
![Figure1: Multi host providing](3-multi-host.png)

## Proxy settings

All proxy rules and options are defined in the **sbe.proxy** file in sbe project root.

    PROXY_HOST="localhost" -> Host or FQDN where is proxy provided PROXY_PORT=80 -> Port where is proxy listen

    PROXY_RULES_WEB=(

            "redmine.localhost=http://redmine.host1/"       -> **Transport rule for HTTP**
            "gerrit.localhost=http://gerrit.host1/"
            "jenkins.localhost=http://jenkins.host1/"
            "nexus.localhost=http://nexus.host1/"

            "redmine.titan.localhost=http://redmine.host2/"
            "gerrit.titan.localhost=http://gerrit.host2/"
            "jenkins.titan.localhost=http://jenkins.host2/"
            "nexus.titan.localhost=http://nexus.host2/"


    )

        PROXY_RULES_SSH=(

            "git.localhost:29418=host1:29418"           -> **Transport rule for SSH**
            "git.titan.localhost:29418=host2:29418"


    )


## Proxy control

Start proxy server

    ./sbe proxy-start


Stop proxy server

    ./sbe proxy-stop


Restart proxy server

    ./sbe proxy-restart


