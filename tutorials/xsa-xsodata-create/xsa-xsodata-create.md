---
title: Creating an OData Service with Create Operation and XSJS Exit
description: Creating an OData Service with Create Operation and XSJS Exit
tags: [  tutorial>intermediate, topic>odata, products>sap-hana, products>sap-hana,-express-edition ]
---
## Prerequisites  
 - **Proficiency:** Intermediate
 - **Tutorials:** [Creating an OData Service with an Entity Relationship](http://go.sap.com/developer/tutorials/xsa-xsodata-entity.html)

## Next Steps
 - [Tutorial Catalog](http://go.sap.com/developer/tutorial-navigator.html)

## Details
### You will learn  
Now to expand your code to include an XSJS exit.

### Time to Complete
**10 Min**.

---

1. Create another OData service named `user2.xsodata` for `dev602.data::User.Details`. This time, also link the create operation to the Server Side JavaScript  Library (XSJSLIB) `xsjs::usersCreateMethod.xsjslib` and the function `usersCreate`. This will be the exit code that performs validation before the insert of the new record. Note: if you don’t want to type this code, we recommend that you cut and paste it from this web address `http://<hostname>:51013/workshop/admin/ui/exerciseMaster/?workshop=dev602&sub=ex3_12`
	
	```
	service namespace "dev602.services"{
	```

2. In the xsjs folder create the file `usersCreateMethod.xsjslib`.  Here is the code for this file. Note: if you don’t want to type this code, we recommend that you cut and paste it from this web address `http://<hostname>:51013/workshop/admin/ui/exerciseMaster/?workshop=dev602&sub=ex3_13`
	
	```
	$.import("xsjs", "session");
	```
	
3. Create another file in the xsjs folder named `session.xsjslib`. Here is the code for this file. Note: if you don’t want to type this code, we recommend that you cut and paste it from this web address `http://<hostname>:51013/workshop/admin/ui/exerciseMaster/?workshop=dev602&sub=ex3_14`

	```
	/**  
	```
	
4. Save and run the Node.js and then the web module. Change the URL to `/xsodata/user2.xsodata` Unfortunately its much more complicated to test Create/Update/Delete methods from the browser as they create other HTTP verbs. Later we will build a user interface which can call this service in order to fully test it.

	![Results](4.png)
## Next Steps
 - [Tutorial Catalog](http://go.sap.com/developer/tutorial-navigator.html)