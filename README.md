# Customer Profile API - Spring Boot Microservices - Teck Task
==============================================================

The main purpose of this sample project is to demonstrate Customer Profile API.
The Customer Profile API provides the ability to Create new profile, update existing profile and delete profile.This project is implemented based on Spring boot Microservices.

There are two Projects

- CRM - Backend application which provides API for consumption
- Customer Profile App - Provides API for Profile management and consumes
  
-------------------------------------------------
 To use this project, you are going to need;

- Java JDK 8 (1.8)
- Maven compatibile with JDK 8
- Java IDE STS/Eclipse
- [Postman tool](https://www.getpostman.com/) (optional, will be used for testing web service)
- Spring 5.0 above
- Webflux library - spring-boot-starter-webflux (Required for backend API consumption)
-------------------------------------------------

Running the Applications
-------------------------------------------------
```
- Customer Profile API

java –jar customer.jar
Base Address: http://127.0.0.1:9091

- CRM API
java –jar crm.jar
Base Address: http://127.0.0.1:9092
```
CUSTOMER PROFILE APP - Following are the API's provided by Profile App.
-----------------------------------------------------------------------
```
#Add new Profile

http://localhost:9091/customer/api/profile

{
"profileId" : "aaaaa",
"firstName" : "Neetha",
"lastName" : "Adehalli",
"dateOfBirth" : "1980-08-20",
"address" : "400, George St, Sydney",
"email" : "neethahjd@shjkas.com",
"phoneNumber" : "+6146832648"
}

response : success/failed
```
-------------------------
```
#UPDATE Profile Request

http://localhost:9091/customer/api/profile/profile1

{
"profileId" : "profile1",
"firstName" : "Neetha",
"lastName" : "HGHGGHG",
"dateOfBirth" : "2080-08-20",
"address" : "400, George st",
"email" : "Test@gmail.com",
"phoneNumber" : "346832648"
}

Response : success/failed

```
------------------------------------------------
```
#GET LIST Profile Request
CRM - GET Profile List Request
http://localhost:9091/customer/api/profile/list

Response
[
   {
        "profileId": "profile1",
        "firstName": " Customer One",
        "lastName": "Li",
        "dateOfBirth": "1982-08-05",
        "address": "400, George st",
        "email": "abc@gmail.com",
        "phoneNumber": "+61436780798"
    },
    {
        "profileId": "profile2",
        "firstName": "Customer Two",
        "lastName": "Lii",
        "dateOfBirth": "1979-07-08",
        "address": "400, George st",
        "email": "xyz@gmail.com",
        "phoneNumber": "+61436781798"
    },
    {
        "profileId": "profile3",
        "firstName": "Customer Three",
        "lastName": "Liii",
        "dateOfBirth": "1985-09-08",
        "address": "400, George st",
        "email": "xyz@gmail.com",
        "phoneNumber": "+61436781798"
    },
    {
        "profileId": "profile4",
        "firstName": "Customer Four",
        "lastName": "Yoo",
        "dateOfBirth": "1988-05-01",
        "address": "400, George st",
        "email": "ytr@gmail.com",
        "phoneNumber": "+61436783798"
    }
]
```
-------------------------------------------------------
```
GET  Single Profile Request
http://localhost:9091/customer/api/profile/get/profile3

  {
        "profileId": "profile3",
        "firstName": "Customer Three",
        "lastName": "Liii",
        "dateOfBirth": "1985-09-08",
        "address": "400, George st",
        "email": "xyz@gmail.com",
        "phoneNumber": "+61436781798"
    }
    
```
-----------------------------------------------------
```
DELETE Profile Request
http://localhost:9091/customer/api/profile/delete/profile3

 {
            "profileId": "profile1",
            "firstName": " Customer One",
            "lastName": "Li",
            "dateOfBirth": "1982-08-05",
            "address": "400, George st",
            "email": "abc@gmail.com",
            "phoneNumber": "+61436780798"
        },
        {
            "profileId": "profile2",
            "firstName": "Customer Two",
            "lastName": "Lii",
            "dateOfBirth": "1979-07-08",
            "address": "400, George st",
            "email": "xyz@gmail.com",
            "phoneNumber": "+61436781798"
        }

```
