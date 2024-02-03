# User API Spec

## Register User API

Endpoint: POST /api/users

Request Body: 
```json
{
    "username": "user",
    "password": "pwd",
    "name": "User 1"
}

```

Response Body Success: 
```json
{
    "data": {
        "username": "user",
        "name": "User 1"
    }
}

```

Response Body Error: 
```json
{
    "errors": "User already registered"
}

```

## Login User API

Endpoint: POST /api/users/login

Request Body: 
```json
{
    "username": "user",
    "password": "pwd",
}

```

Response Body Success: 
```json
{
    "data": {
        "token": "unique-token",
    }
}

```

Response Body Error: 
```json
{
    "errors": "Username or password wrong"
}

```

## Update User API

Endpoint: PATCH /api/users/current

Headers: 
- Authorization : token

Request Body: 
```json
{
    "name": "Nama Baru",
    "password": "new pwd",
}

```

Response Body Success: 
```json
{
    "data": {
        "name": "Nama Baru",
        "username": "user"
    }
}

```

Response Body Error: 
```json
{
    "errors": "Username or password wrong"
}

```

## Get User API

Endpoint: GET /api/users/current

Headers: 
- Authorization : token

Response Body Success: 
```json
{
    "data": {
        "username": "user",
        "name": "Nama Baru"
    }
}

```

Response Body Error: 
```json
{
    "errors": "Unauthorized"
}

```

## Logout User API

Endpoint: DELETE /api/users/logout

Response Body Success:

```json
{
    "data": "OK"
}

```

Response Body Error: 
```json
{
    "errors": "User tidak login"
}

```