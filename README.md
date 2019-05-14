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
  "Profile":[
    {
      "_id": 34dtg3ea235223,
      "name":"table1",
      "page_name": "page_name",
      "email": email@emil.com,
      "phone":"0989990",
      "logo":"url",
      "admin_password":"123456",
      "type":"res",
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
            "_id": "5cdaaa12315b41f55085ee09",
            "name": "name1",
            "uptime": "14/05/2019"
        },
        {
            "_id": "5cdaaa1a315b41f55085ee0a",
            "name": "name3",
            "uptime": "14/05/2019"
        },
        {
            "_id": "5cdaaa1c315b41f55085ee0b",
            "name": "name2",
            "uptime": "14/05/2019"
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
            "_id": "5cdab0b526139a06a5da8637",
            "user_id": "5cda9cdafbf39b10146bd006",
            "table_id": "5cdaaa1c315b41f55085ee0b",
            "name": "rasheed",
            "age": "19/05/2020",
            "email": "email@email",
            "phone": "1234567",
            "service": 4.5,
            "cleanliness": 3.3,
            "food_assessment": 4,
            "wc": 5,
            "atmosphere": 2,
            "recommended": true,
            "dishes": "sdsdsdsdsd",
            "uptime": "14/05/2019, 3:12:37 pm",
            "__v": 0
        },
        {
            "_id": "5cdab0b726139a06a5da8638",
            "user_id": "5cda9cdafbf39b10146bd006",
            "table_id": "5cdaaa1c315b41f55085ee0b",
            "name": "rasheed",
            "age": "19/05/2020",
            "email": "email@email",
            "phone": "1234567",
            "service": 4.5,
            "cleanliness": 3.3,
            "food_assessment": 4,
            "wc": 5,
            "atmosphere": 2,
            "recommended": true,
            "dishes": "sdsdsdsdsd",
            "uptime": "14/05/2019, 3:12:39 pm",
            "__v": 0
        }
    ]
}
```

