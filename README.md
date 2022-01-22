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
METHOD: GET
URI:address/api/roles

-**Register user**
METHOD: POST
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
METHOD: POST
URI:address/api/signout

-**User login**
METHOD: POST
URI:address/api/signin
BODY SAMPLE:{
    "username": "Yogona",
    "password": "1234",
    "device_name": "HUAWEI"
}

**User**
-**View User**
METHOD: GET
URI: address/api/profile/{id}
EXAMPLE: localhost:8000/api/profile/1

-**Update User**
METHOD: PUT
URI: address/api/profile/user/update/{user_id}
EXAMPLE: localhost:8000/api/profile/user/update/1
BODY SAMPLE: {
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
METHOD: DELETE
URI: address/api/profile/user/delete/{user_id}
EXAMPLE: localhost:8000/api/profile/user/delete/1

-**Disable User**
METHOD: PATCH 
URI: address/api/profile/user/disable/{user_id}
EXAMPLE: localhost:8000/api/profile/user/disable/1

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
URI: address/api/profile/payment/view/{profile_id}
EXAMPLE: localhost:8000/api/profile/payment/view/1

-**Update Profile**
METHOD: PUT
URI: address/api/profile/payment/update/{profile_id}
EXAMPLE: address/api/profile/payment/update/1

-**Delete Profile**
METHOD: DELETE
URI: address/api/profile/payment/delete/{profile_id}
EXAMPLE: address/api/profile/payment/delete/1
