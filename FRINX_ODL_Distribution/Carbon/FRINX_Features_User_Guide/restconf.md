[Documentation main page](https://frinxio.github.io/Frinx-docs/)
[FRINX Features User Guide main page](https://frinxio.github.io/Frinx-docs/FRINX_ODL_Distribution/Carbon/user_guide.html)
# RESTCONF

<!-- TOC START min:1 max:3 link:true update:true -->
- [RESTCONF](#restconf)
  - [RESTCONF operations overview](#restconf-operations-overview)
  - [Mount point](#mount-point)
  - [HTTP methods](#http-methods)
    - [OPTIONS /restconf](#options-restconf)
    - [GET /restconf/config/&lt;identifier&gt;](#get-restconfconfigltidentifiergt)
    - [GET /restconf/operational/&lt;identifier&gt;](#get-restconfoperationalltidentifiergt)
    - [PUT /restconf/config/&lt;identifier&gt;](#put-restconfconfigltidentifiergt)
    - [POST /restconf/config](#post-restconfconfig)
    - [POST /restconf/config/&lt;identifier&gt;](#post-restconfconfigltidentifiergt)
    - [POST /restconf/operations/&lt;moduleName&gt;:&lt;rpcName&gt;](#post-restconfoperationsltmodulenamegtltrpcnamegt)
    - [DELETE /restconf/config/&lt;identifier&gt;](#delete-restconfconfigltidentifiergt)

<!-- TOC END -->
## RESTCONF operations overview
RESTCONF allows access to datastores in the controller.  
There are two datastores:  
**Config**: Contains data inserted via the controller  
**Operational**: Contains other data  

*Note:Each request must start with the URI /restconf.
RESTCONF listens on port 8080 for HTTP requests.*

RESTCONF supports **OPTIONS**, **GET**, **PUT**, **POST**, and **DELETE** operations. Request and response data can either be in the XML or JSON format. XML structures according to yang are defined at: [XML-YANG](https://tools.ietf.org/html/rfc6020). JSON structures are defined at: [JSON-YANG](https://tools.ietf.org/html/draft-lhotka-netmod-yang-json-02). Data in the request must have a correctly set Content-Type field in the http header with the allowed value of the media type. The media type of the requested data has to be set in the Accept field. Get the media types for each resource by calling the OPTIONS operation. Most of the paths of the pathsRestconf endpoints use [Instance Identifier](https://wiki.opendaylight.org/view/OpenDaylight_Controller:MD-SAL:Concepts#Instance_Identifier). **&lt;identifier&gt;** is used in the explanation of the operations.

**&lt;identifier&gt;**
* This must start with &lt;moduleName&gt;:&lt;nodeName&gt;&gt; where &lt;moduleName&gt; is a name of the module and &lt;nodeName&gt; is the name of a node in the module. It is sufficient to just use &lt;nodeName&gt; after &lt;moduleName&gt;:&lt;nodeName&gt;. Each &lt;nodeName&gt; has to be separated by /.

* &lt;nodeName&gt; can represent a data node which is a list or container yang built-in type. If the data node is a list, there must be defined keys of the list behind the data node name, for example, &lt;nodeName&gt;/&lt;valueOfKey1&gt;/&lt;valueOfKey2&gt;.

* The format &lt;moduleName&gt;:&lt;nodeName&gt; has to be used in this case as well:  
Module A has node A1. Module B augments node A1 by adding node X. Module C augments node A1 by adding node X. For clarity, it has to be known which node is X (for example: C:X). For more details about encoding, see: [RESTCONF 02 - Encoding YANG Instance Identifiers in the Request URI](https://tools.ietf.org/html/draft-bierman-netconf-restconf-02#section-5.3.1).

## Mount point
A Node can be behind a mount point. In this case, the URI has to be in the format &lt;identifier&gt;/yang-ext:mount/&lt;identifier&gt;. The first &lt;identifier&gt; is the path to a mount point and the second &lt;identifier&gt; is the path to a node behind the mount point. A URI can end in a mount point itself by using &lt;identifier&gt;/yang-ext:mount.  
More information on how to actually use mountpoints is available at: [OpenDaylight Controller:Config:Examples:Netconf](https://wiki.opendaylight.org/view/OpenDaylight_Controller:Config:Examples:Netconf).

## HTTP methods
### OPTIONS /restconf  
* Returns the XML description of the resources with the required request and response media types in Web Application Description Language (WADL)

### GET /restconf/config/&lt;identifier&gt;  
* Returns a data node from the Config datastore.
* &lt;identifier&gt; points to a data node which must be retrieved.

### GET /restconf/operational/&lt;identifier&gt;
* Returns the value of the data node from the Operational datastore.
* &lt;identifier&gt; points to a data node which must be retrieved.

### PUT /restconf/config/&lt;identifier&gt;
* Updates or creates data in the Config datastore and returns the state about success.
* &lt;identifier&gt; points to a data node which must be stored.

Example:  
```
PUT http://<controllerIP>:8080/restconf/config/module1:foo/bar
Content-Type: applicaton/xml
<bar>
  …
</bar>
```
Example with mount point:  
```
PUT http://<controllerIP>:8080/restconf/config/module1:foo1/foo2/yang-ext:mount/module2:foo/bar
Content-Type: applicaton/xml
<bar>
  …
</bar>
```
### POST /restconf/config
Creates the data if it does not exist  

Example:  
```
POST URL: http://localhost:8080/restconf/config/
content-type: application/yang.data+json
JSON payload:

   {
     "toaster:toaster" :
     {
       "toaster:toasterManufacturer" : "General Electric",
       "toaster:toasterModelNumber" : "123",
       "toaster:toasterStatus" : "up"
     }
  }
```
### POST /restconf/config/&lt;identifier&gt;
* Creates the data if it does not exist in the Config datastore, and returns the state about success.
* &lt;identifier&gt; points to a data node where data must be stored.
* The root element of data must have the namespace (data are in XML) or module name (data are in JSON.)

Example:  
```
POST http://<controllerIP>:8080/restconf/config/module1:foo
Content-Type: applicaton/xml/
<bar xmlns=“module1namespace”>
  …
</bar>
```
Example with mount point:  
```
http://<controllerIP>:8080/restconf/config/module1:foo1/foo2/yang-ext:mount/module2:foo
Content-Type: applicaton/xml
<bar xmlns=“module2namespace”>
  …
</bar>
```
### POST /restconf/operations/&lt;moduleName&gt;:&lt;rpcName&gt;
* Invokes RPC.
* &lt;moduleName&gt;:&lt;rpcName&gt; - &lt;moduleName&gt; is the name of the module and &lt;rpcName&gt; is the name of the RPC in this module.
* The Root element of the data sent to RPC must have the name “input”.  
* The result can be the status code or the retrieved data having the root element “output”.  

Example:  
```
POST http://<controllerIP>:8080/restconf/operations/module1:fooRpc
Content-Type: applicaton/xml
Accept: applicaton/xml
<input>
  …
</input>
```
The answer from the server could be:  
```
<output>
  …
</output>
```
An example using a JSON payload:  
```
POST http://localhost:8080/restconf/operations/toaster:make-toast
Content-Type: application/yang.data+json
{
  "input" :
  {
     "toaster:toasterDoneness" : "10",
     "toaster:toasterToastType":"wheat-bread"
  }
}
```
*Note
Even though this is a default for the toasterToastType value in the yang, you still need to define it.*  

### DELETE /restconf/config/&lt;identifier&gt;
* Removes the data node in the Config datastore and returns the state about success.
* &lt;identifier&gt; points to a data node which must be removed.
More information is available in the [RESTCONF RFC](https://tools.ietf.org/html/draft-bierman-netconf-restconf-02).


*Credit for the content of this page goes to the OpenDaylight community. The page content is take from [here](http://docs.opendaylight.org/en/stable-carbon/developer-guide/controller.html?highlight=restconf#opendaylight-controller-md-sal-restconf)*
