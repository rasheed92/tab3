# tab3


### Login 
Link:[/api/v1/auth/login/]()
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
Link:[/api/v1/auth/registration/]()
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
phone: Required
<br><br>
logo: Required
<br><br>
admin_password: Required
<br><br>
Response :
```
{
    "msg": "add..",
}
```

### Get Profile 
Link:[api/v1/auth/me]()
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
Link:[api/v1/table/]()
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
  "tables":[
    {
      "_id": 34dtg3ea235223,
      "name":"table1",
    },
      {
      "_id": 34dtg3ea235223,
       "name":"table2",
    }
    ]
}
```

### delete table 
Link:[/api/v1/table/delete/:id]()
<br><br>
**headers**
<br><br>
token: Required
<br><br>
Method: **POST**	
Response :
```
{
  "msg":"table has been delete"
}

```
### add table 
Link:[/api/v1/table/add/]()
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
Response :
```
{
  "msg":"table has been add"
}

```

### add servey 
Link:[/api/v1/servey/add/]()
<br><br>
**headers**
<br><br>
token: Required
<br><br>
Method: **POST**	
<br><br>
**BODY**
food:Required||folt,
<br><br>
sevice:Required,
<br><br>
food:Required||folt,
<br><br>
clean:Required||folt,
<br><br>
wc:Required||folt,
<br><br>
Ajowaa:Required||folt,
<br><br>
Would:Required||boolean,
<br><br>
name:Required||string,
<br><br>
email:Required||string,
<br><br>
age:Required||string||13/05/2019,
<br><br>
phone:Required||string,
Response :
```
{
  "msg":"servey has been add"
}

```
### Get servey 
Link:[api/v1/servey/table_id]()
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
  "servey":[
    {
    _id:"232adawd2232323"
     food:4.5
    "sevice":4,
    "food":4.5,
    "clean":5,
    "wc":5,
    "ajowaa":3.5,
    "would":true,
    "name":"m63am",
    "email":"email@email",
    "age":"13/05/2019",
    "phone":"12341",
    },
        {
    _id:"232adawd2252323"
     food:4.5
    "sevice":4,
    "food":4.5,
    "clean":5,
    "wc":5,
    "ajowaa":3.5,
    "would":true,
    "name":"m63am",
    "email":"email@email",
    "age":"13/05/2019",
    "phone":"12341",
    },
        {
    _id:"232adawd332323"
     food:4.5
    "sevice":4,
    "food":4.5,
    "clean":5,
    "wc":5,
    "ajowaa":3.5,
    "would":true,
    "name":"m63am",
    "email":"email@email",
    "age":"13/05/2019",
    "phone":"12341",
    },
    
    ]
}



