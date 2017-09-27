You can use this guide to help you identify and resolve basic problems you may experience with your SBE instance.

Each SBE container has the following pre-installed tools:

    netcat  
    ssh-client  
    ssh-server  
    telnet  
    

**SSH login credentials for each container:**

username: admin  
password: admin

Example of SSH login into "apache-ds" component container:

    docker exec -it sbe-default-gerrit service ssh start
    ssh admin@<component-ip>
    

Note the SSHd service is not enabled by default for each component
