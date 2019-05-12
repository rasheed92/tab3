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
phone_number: Required
<br><br>
Tables_number: Required
<br><br>
type : Required
<br><br>
Response :
```
{
    "msg": "add..",
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
      "id": 34dtg3ea235223,
      "name":"table1",
    },
      {
      "id": 34dtg3ea235223,
       "name":"table2",
    }
    ]
}
```

### delete table 
Link:[/api/v1/table/delete/]()
<br><br>
**headers**
<br><br>
token: Required
<br><br>
Method: **POST**	
<br><br>
**BODY**
<br><br>
table_id: Required
<br><br>
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
Response :
```
{
  "msg":"table has been add"
}

```




