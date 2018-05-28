# API
## Users
### [post] /api/register
Body:
```
{
  "name": "required",
  "email": "email|required",
  "password": "required",
  "c_password": "required|same:password"
}
```
Response success: HTTP 200
```
{
  "success": {
    "id": "user_id",
    "token": "user_token",
    "name": "user_name"
  }
}
```
Response error: HTTP 401
```
{
  "error": "Unauthorised"
}
```

### [post] /api/login
Body
```
{
  "email": "email|required",
  "password": "required"
}
```
Response success: HTTP 200
```
{
  "success": {
    "token": "user_token"
  }
}
```
Response error: HTTP 401
```
{
  "error": "Unauthorised"
}
```
### [get] /api/details
Response success: HTTP 200
```
{
  "success": {
    "id": 1,
        "name": "Jayr Editado",
        "email": "jayr@jayr.com",
        "password": "$2y$10$WGOqp8kvDKHrYAVbKP0K9.rDiL/i8wK8eFyK6lRoX95FVdRWmRwQC",
        "remember_token": null,
        "created_at": "2018-05-28 18:42:51",
        "updated_at": "2018-05-28 18:56:59"
  }
}
```
Response error: HTTP 401
```
{
  "error": "Unauthorised"
}
```
### [put] /api/edit/{id}
@param id {int}

Response success: HTTP 200
```
{
  "success": "Editado com sucesso"
}
```
Response error: HTTP 401
```
{
  "error": "Unauthorised"
}
```
