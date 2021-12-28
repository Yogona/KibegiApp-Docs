# kibegi-backend
The whole skeleton of how the system is structured for storage, authentication and authorization from the backend perspective.

**Warning!**
-Before you exploit these useful API features, please checkout kibegi-physical-schema and kibegi-ERD files. 

**How to use  API features**
All the uris developed have auth and authorization scopes except some of them, to be discussed further below.

**RESPONSE FORMAT, JSON:**
-status
-message
-body

**Authentication**
-**Get roles**
METHOD:get
URI:address/api/roles

-**Register user**
METHOD:post
URI:address/api/register

-**User login**
