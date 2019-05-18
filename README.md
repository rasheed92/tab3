# tab3


### Login 
Link:[/api/v1/auth/login/](https://tab3.herokuapp.com/api/v1/auth/login/)
<br><br>
Method: **POST**	
<br><br>
**BODY**
<br><br>
email: Required
<br><br>
password: Required
<br><br>
Response :
```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjODE1NmY4NjA3M2U3NTU1MDhlZDNjMiIsImlhdCI6MTU1MjY1NTIwMSwiZXhwIjoxNTU1MDc0NDAxfQ.gTX4y6LrEWHOSFWk60lHzrdTeV3K10iXpTLbAN2nNCc",
}
```


### Registration 
Link:[/api/v1/auth/registration/](https://tab3.herokuapp.com/api/v1/auth/registration/)
<br><br>
Method: **POST**	
<br><br>
**BODY**
<br><br>
email: Required
<br><br>
password: Required
<br><br>
name: Required
<br><br>
page_name: Required
<br><br>
phone: Required
<br><br>
logo: Required
<br><br>
admin_password: Required
<br><br>
discount: Required
<br><br>
license: Required||date
<br><br>
Response :
```
{
    "msg": "add..",
}
```

### Get Profile 
Link:[api/v1/auth/me](https://tab3.herokuapp.com/api/v1/auth/me/)
<br><br>
Method: **GET**	
<br><br>
**headers**
<br><br>
token:Required
<br><br>
Response :
```
{
    "profile": [
        {
            "_id": "5cdff0df83b50e0c18b438e6",
            "email": "user@user",
            "adminPassword": "12345678",
            "name": "user@user",
            "phone": "1234567",
            "comp_id": {
                "_id": "5cdfedeeee2f4922c013bc1b",
                "email": "m@m.com",
                "name": "m63am",
                "page_name": "@m63am",
                "phone": "1234567",
                "discount": 25,
                "type": "res",
                "logo": "fe8d86a0-7960-11e9-9a40-e92308315370681658c0-7571-11e9-aa5f-19197b7c69d030cd8890-72a4-11e9-ac23-bddb103e8a2e63b57bd0-72a1-11e9-82a4-1b567eac89f3074ef6a0-6f90-11e9-9b6b-4d4c1d0495382222446_c673.jpg",
                "uptime": "18/05/2019",
                "__v": 0
            },
            "type": "res",
            "licenseDate": "2019-07-14",
            "uptime": "18/05/2019"
        }
    ]
}
```
### Get Tables 
Link:[api/v1/table/](https://tab3.herokuapp.com/api/v1/table/)
<br><br>
Method: **GET**	
<br><br>
**headers**
<br><br>
token:Required
<br><br>
Response :
```
{
    "tables": [
        {
            "_id": "5cde0780a2c67a2b382cea72",
            "name": "name 4",
            "last_rating": 4.2,
            "rating": 4.05,
            "red": false,
            "uptime": "17/05/2019"
        },
        {
            "_id": "5cde0785a2c67a2b382cea73",
            "name": "name 1",
            "last_rating": 0,
            "rating": 0,
            "red": false,
            "uptime": "17/05/2019"
        },
        {
            "_id": "5cde0787a2c67a2b382cea74",
            "name": "name 2",
            "last_rating": 0,
            "rating": 0,
            "red": false,
            "uptime": "17/05/2019"
        },
        {
            "_id": "5cde078aa2c67a2b382cea75",
            "name": "name 3",
            "last_rating": 0,
            "rating": 0,
            "red": false,
            "uptime": "17/05/2019"
        }
    ]
}
```

### delete table 
Link:[/api/v1/table/delete](https://tab3.herokuapp.com/api/v1/table/delete)
<br><br>
**headers**
<br><br>
token: Required
<br><br>
<br><br>
Method: **POST**
<br><br>
**body**
table_id: Required
<br><br>
Response :
```
{
  "msg":"table has been delete"
}

```
### add table 
Link:[/api/v1/table/add/](https://tab3.herokuapp.com/api/v1/table/add/)
<br><br>
**headers**
<br><br>
token: Required
<br><br>
Method: **POST**	
<br><br>
**BODY**
<br><br>
name: Required
<br><br>
Response :
```
{
  "msg":"table has been add"
}

```

### add servey 
Link:[/api/v1/servey/add/](https://tab3.herokuapp.com/api/v1/servey/add/)
<br><br>
**headers**
<br><br>
token: Required
<br><br>
Method: **POST**	
<br><br>
**BODY**
<br><br>
table_id:Required,
<br><br>
food_assessment:Required||float,
<br><br>
service:Required||float,
<br><br>
cleanliness:Required||float,
<br><br>
wc:Required||float,
<br><br>
atmosphere:Required||float,
<br><br>
recommended:Required||boolean,
<br><br>
name:Required||string,
<br><br>
dishes:Required||string,
<br><br>
email:Required||string,
<br><br>
age:Required||string||13/05/2019,
<br><br>
phone:Required||string,
<br><br>
**people_number:Required||number,**
<br><br>
Response :
```
{
  "msg":"servey has been add"
}

```
### Get servey 
Link:[api/v1/servey/table_id](https://tab3.herokuapp.com/api/v1/survey/table/5cdaaa1c315b41f55085ee0b)
<br><br>
Method: **GET**	
<br><br>
**headers**
<br><br>
token:Required
<br><br>
Response :
```
{
    "survey": [
        {
            "_id": "5cde0a8dac106243c48310a9",
            "user_id": "5cddecccb57c6446044fb8ae",
            "table_id": "5cde0780a2c67a2b382cea72",
            "name": "rasheed",
            "age": "19/05/2020",
            "email": "email@email",
            "phone": "1234567",
            "service": 4,
            "people_number": 4,
            "cleanliness": 5,
            "food_assessment": 5,
            "wc": 5,
            "atmosphere": 2,
            "recommended": true,
            "dishes": "sdsdsdsdsd",
            "uptime": "17/05/2019, 4:12:45 am",
            "__v": 0
        },
        {
            "_id": "5cde0a201350e642cccbb987",
            "user_id": "5cddecccb57c6446044fb8ae",
            "table_id": "5cde0780a2c67a2b382cea72",
            "name": "rasheed",
            "age": "19/05/2020",
            "email": "email@email",
            "phone": "1234567",
            "service": 4,
            "people_number": 4,
            "cleanliness": 5,
            "food_assessment": 5,
            "wc": 5,
            "atmosphere": 2,
            "recommended": true,
            "dishes": "sdsdsdsdsd",
            "uptime": "17/05/2019, 4:10:56 am",
            "__v": 0
        },
        {
            "_id": "5cde09e11350e642cccbb986",
            "user_id": "5cddecccb57c6446044fb8ae",
            "table_id": "5cde0780a2c67a2b382cea72",
            "name": "rasheed",
            "age": "19/05/2020",
            "email": "email@email",
            "phone": "1234567",
            "service": 4,
            "people_number": 4,
            "cleanliness": 5,
            "food_assessment": 4,
            "wc": 3,
            "atmosphere": 2,
            "recommended": true,
            "dishes": "sdsdsdsdsd",
            "uptime": "17/05/2019, 4:09:53 am",
            "__v": 0
        }
    ]
}
```

