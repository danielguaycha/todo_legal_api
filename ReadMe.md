# TodoLegal Service
## Requirements
Check `requirements.txt`, this service is build with python 3.9.5

## libs
```bash
pip install Django==3.2.4
pip install django-rest-knox==4.1.0
pip install djangorestframework==3.12.4
pip install django-cors-headers==3.7.0
```
## Migrate
```bash
py manage.py migrate
```

## Run
```bash
py manage.py runserver
```

## ApiDoc
### Register user
POST: `/api/user/`

Allow: POST, OPTIONS\
Content-Type: application/json\
Vary: Accept\

**Request**
```json
{
    "first_name":  "FistName",
    "last_name": "LastName",
    "email": "mail@mail.com",
    "username": "0706271301",
    "password": "12345678"
}
```
**Response**
```json
{
    "status": "Ok",
    "user": {
        "id": 9,
        "username": "0706271285",
        "first_name": "FistName",
        "last_name": "LastName",
        "email": "mail@mail.com"
    },
    "token": "558ecda258cd408c5967c1a8571d808d50bd499712a4ccc06cee7e4eb280df20"
}
```
***
### Login User
GET `/api/login/`

Allow: POST, OPTIONS\
Content-Type: application/json\
Vary: Accept

**Request**
```json
{
    "username": "0706271301",
    "password": "12345678"
}
```
**Response**
```json
{
    "status": "Ok",
    "user": {
        "id": 2,
        "username": "0706271301",
        "first_name": "Daniel",
        "last_name": "Guaycha",
        "email": "danielguaycha@gmail.com"
    },
    "token": "0917433a3d176ff119ca641c62e933a5da35e9ad06519d28c6b2b2762263a573"
}
```



