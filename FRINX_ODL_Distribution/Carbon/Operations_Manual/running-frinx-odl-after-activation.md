[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[Operations Manual main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Carbon/operations_manual.html)
# Running the FRINX ODL distribution after initial activation

After running for the first time and generating a local license file, you no longer need to provide a token when starting karaf.
The following oeprations have been tested in CentOS and Ubuntu 16.04.

## Operating karaf in the foreground
### Starting karaf
In your Frinx ODL Distribution directory, for example /home/username/distribution-karaf-3.1.0.frinx, type

    ./bin/karaf 

### Stopping karaf
To stop from within the karaf console there are three options:

1. Hold the 'CTRL' key and press the 'd' key 
2. Type:
```
    halt
```
3. Type:
```
    system:shutdown
```
When prompted to confirm, type 'yes'.

## Operating karaf in the background
### Starting karaf 
In your Frinx ODL Distribution directory, for example /home/username/distribution-karaf-3.1.0.frinx, type
```
    ./bin/start
```
### Confirming karaf is running
Type
```
    ./bin/status
```
### Connecting to the background process
Type
```
    ./bin/client
```
or type
```
    ssh karaf@localhost -p 8101
```
(password: karaf)

### Stopping karaf
Type
```
    ./bin/stop
```
## Resetting FRINX ODL
To 'reset' your distribution to a clean state and delete any features previously installed type the following within your frinx ODL distribution directory (e.g. /home/username/distribution-karaf-3.1.0.frinx)
```
    rm -rf /data /cache /journal
```
## Setting JAVA_HOME and other variables
This is done by editing the 'setenv' file in the bin directory. Uncommenting the relevant line and set the variable as required e.g.:
``` 
    export JAVA_HOME=/opt/jdk1.8.0_151
```