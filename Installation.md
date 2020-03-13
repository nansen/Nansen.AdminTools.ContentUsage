# Nansen.AdminTools.ContentUsage
#### v1.1.0
## Installation
------------

Installation is done as a standard nuget package install. The required views for the Find Content Usages admin tool are 
added under modules/_protected. 

An update to the Web.config file is required for the module to run correctly. It is detailed below.


## Update Web.config
-----------------
In order to give access to the modules/_protected folder, the `<protectedModule>` node under `<episerver.shell>` in your web.config
must be updated to add the new module. This will be done automatically upon installation using transforms. The resulting configuration will have
the following added: 

```xml
<add name="NansenContentUsage" />
```