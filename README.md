# cmpe273-lab2
CMPE 273 lab2

## Python Flask application

### REST Endpoints implemented.

* Create a new student

```
POST /students

# Request
{
    "name": "Bob Smith"
}

# Response
# HTTP Code: 201
{
    "id" : 1234456,
    "name" : "Bob Smith"
}
```

* Retrieve an existing student

```
GET /students/{id}

{
    "id" : 1234456,
    "name" : "Bob Smith"
}
```

* Create a class

```
POST /classes

# Request
{
    "name": "CMPE-273"
}

# Response
{
    "id": 1122334,
    "name": "CMPE-273",
    "students": []
}
```

* Retrieve a class

```
GET /classes/{id}

{
    "id": 1122334,
    "name": "CMPE-273",
    "students": []
}
```

* Add students to a class

```
PATCH /classes/{id}

# Request
{
    "student_id": 1234456
}

# Response
{
    "id": 1122334,
    "name": "CMPE-273",
    "students": [
        {
            "id" : 1234456,
            "name" : "Bob Smith"
        }
    ]
}

```