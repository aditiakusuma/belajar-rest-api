# Contact API Spec

## Create Contact API
Endpoint: POST /api/contacts

Headers:
- Authorization: token

Request Body:

```json
{
    "first_name": "Aditia",
    "last_name": "Kusuma",
    "email": "aditiakusuma@gmail.com",
    "phone": "08856678678"
}
```

Response Body Success:

```json
{
    "data": {
        "id": 1,
        "first_name": "Aditia",
        "last_name": "Kusuma",
        "email": "aditiakusuma@gmail.com",
        "phone": "08856678678"
    }
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```

## Update Contact API

Endpoint: PUT /api/contacts/:id

Headers:
- Authorization: token

Request Body:

```json
{
    "first_name": "Aditia",
    "last_name": "Kusuma",
    "email": "aditiakusuma@gmail.com",
    "phone": "08856678678"
}
```

Response Body Success:

```json
{
    "data": {
        "id": 1,
        "first_name": "Aditia",
        "last_name": "Kusuma",
        "email": "aditiakusuma@gmail.com",
        "phone": "08856678678"
    }
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```

## Get Contact API

Endpoint: POST /api/contacts?;id

Headers:
- Authorization: token

Response Body Success:

```json
{
    "data": {
        "id": 1,
        "first_name": "Aditia",
        "last_name": "Kusuma",
        "email": "aditiakusuma@gmail.com",
        "phone": "08856678678"
    }
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```

## Search Contact API


Endpoint: GET /api/contacts

Headers:
- Authorization: token


Query params:
- name: Search by first_name or last_name, using like, optional
- email: Search by email using like, optional
- phone: Search by phone using like, optional
- page: number of page, default 1
- size: size per page, default 10

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
    "pagination": {
        "page": 1,
        "size": 10
    }
}
```

Response Body Error:

```json
{
    "errors": "Message",
}
```

## Remove Contact API

Endpoint: DELETE /api/contacts/:id

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