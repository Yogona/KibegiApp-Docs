# kibegi-backend
The whole skeleton of how the system is structured for storage, authentication and authorization from the backend perspective.

**Warning!**
-Before you exploit these useful API features, please checkout kibegi-physical-schema and kibegi-ERD files. 

**How to use  API features**
All the URIs developed have auth and authorization scopes except some of them, to be discussed further below.

--To send requests you must include user token in the header as bearer token--

**RESPONSE FORMAT, JSON:**
-status->Status code.
-message->Status message.
-body->Body of the feedback.

**Authentication**
No authentication and authorization checks.

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

**User**
-**View User**
METHOD: get
URI: address/api/profile/{id}

-**Update User**
METHOD: put
URI: address/api/profile/user/update
BODY SAMPLE: {
    "id": 1,
    "f_name": "Yona",
    "m_name": "Godwin",
    "l_name": "Yona",
    "gender": "M",
    "nationality": "Tanzanian",
    "email": "yonagodwin@gmail.com",
    "phone": "0712500282",
    "address": "Dodoma"
}

-**Delete User**
METHOD: delete
URI: address/api/profile/user/delete
BODY SAMPLE: {
    "user_id": "1"
}

-**Disable User**
METHOD: put 
URI: address/api/profile/user/disable
BODY SAMPLE: {
    "user_id": "1"
}

**Payment Profile**
-**Add Profile**
METHOD: POST
URI: address/api/profile/payment/add
BODY SAMPLE: {
    "payment_name": "Paypal",
    "client_names": "Yona Godwin",
    "address_one": "Dodoma",
    "address_two": "",
    "acc_id": "yonagodwin@gmail.com"
}

-**View Profiles**
METHOD: GET
URI: address/api/profile/payment/view

-**View Profile**
METHOD: GET
URI: address/api/profile/payment/view/{id}
