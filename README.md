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
    "username": "Yogona",
    "password": "1234",
    "f_name": "Yona",
    "m_name": "Godwin",
    "l_name": "Yona",
    "gender": "M",
    "nationality": "Tanzanian",
    "email": "yonagodwin@gmail.com",
    "phone": "0712500282",
    "address": "Dodoma",
    "role_id": "1",
    "device_name": "HUAWEI"
}

-**User login**
