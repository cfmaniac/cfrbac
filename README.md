Simple Role Based Access Control for Coldfusion ORM
===================================================

_Currently a work in progress_
------------------------------

###Concept

Give any entity that can perform actions, typically a User entity an property "Roles" 
	
```Coldfusion
property name="Roles" fieldtype="many-to-many" 
	singularname="Role" cfc="net.m0nk3y.cfrbac.entity.Role" 
	linktable="tests_UserRoles"; 
```

Then include a mixin that will provide the functions used to evaluate permissions

```coldfusion
include "/net/m0nk3y/cfrbac/mixins/can.cfm"; 
```

Include "/net/m0nk3y/cfrbac/entity" in your applications orm cfclocations

```cfml
this.ormsettings.cfclocation = ["/net/m0nk3y/cfrbac/entity", "/my/model/cfcs"]
```




