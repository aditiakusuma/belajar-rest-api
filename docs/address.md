# Address API Spec

## Create Address API
Endpoint: POST /api/contacts/:contactId/addresses

Headers:
- Authorization: token

Request Body:

```json
{
    "street": "Jl. khdfkdka",
    "city": "Kusuma",
    "province": "aditiakusuma@gmail.com",
    "country": "08856678678",
    "postal_code": "67576"
}
```

Response Body Success:

```json
{
    "data": {
        "id": 1,
        "street": "Jl. khdfkdka",
        "city": "Kusuma",
        "province": "aditiakusuma@gmail.com",
        "country": "08856678678",
        "postal_code": "67576"
    }
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```

## Update Address API

Endpoint: PUT /api/contacts/:contactId/addresses/:addressId

Headers:
- Authorization: token

Request Body:

```json
{
    "street": "Jl. khdfkdka",
    "city": "Kusuma",
    "province": "aditiakusuma@gmail.com",
    "country": "08856678678",
    "postal_code": "67576"
}
```

Response Body Success:

```json
{
    "data": {
        "id": 1,
        "street": "Jl. khdfkdka",
        "city": "Kusuma",
        "province": "aditiakusuma@gmail.com",
        "country": "08856678678",
        "postal_code": "67576"
    }
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```

## List Address API


Endpoint: GET /api/contacts/:contactId/addresses

Headers:
- Authorization: token

Response Body Success:

```json
{
    "data": [
        {
            "id": 1,
            "first_name": "Aditia",
            "last_name": "Kusuma",
            "email": "aditiakusuma@gmail.com",
            "phone": "08856678678"
        },
        {
            "id": 2,
            "first_name": "Aditia",
            "last_name": "Kusuma",
            "email": "aditiakusuma@gmail.com",
            "phone": "08856678678"
        }
    ],
    
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```

## Remove Address API

Endpoint: DELETE /api/contacts/:contactId/address/:addressId

Headers:
- Authorization: token


Response Body Success:

```json
{
    "data": "OK"
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```