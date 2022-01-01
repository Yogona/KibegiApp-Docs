# kibegi-backend
The whole skeleton of how the system is structured for storage, authentication and authorization from the backend perspective.

**Warning!**
-Before you exploit these useful API features, please checkout kibegi-physical-schema and kibegi-ERD files. 

**How to use  API features**
All the URIs developed have auth and authorization scopes except some of them, to be discussed further below.

**RESPONSE FORMAT, JSON:**
-status->Status code.
-message->Status message.
-body->Body of the feedback.

**Authentication**
-**Get roles**
METHOD:get
URI:address/api/roles

-**Register user**
METHOD:post
URI:address/api/register
BODY SAMPLE:{
    "username": "John",
    "password": "1234",
    "f_name": "John",
    "m_name": "",
    "l_name": "Doe",
    "gender": "M",
    "nationality": "Ukranian",
    "email": "contact@tansoften.com",
    "phone": "0713500280",
    "address": "Arusha",
    "role_id": "1",
    "device_name": "SAMSUNG"
}

-**Logout user**
METHOD:post
URI:address/api/signout
BODY SAMPLE:{
    "user_id":"2"
}

-**User login**
METHOD:post
URI:address/api/signin
BODY SAMPLE:{
    "username": "Yogona",
    "password": "1234",
    "device_name": "HUAWEI"
}
