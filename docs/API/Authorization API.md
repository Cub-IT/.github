# That document describes API that is used by clients to interact with CubIT

### POST /api/v1/user/new
Registration

#### Request body:
```
{
	“userFirstName”:  string,
	“userLastName”:   string,
	“email”:          string,
	“password”:       string
}
```

#### Example:

```
curl --location --request POST 'https://cub.it/api/v1/user/new' \
--header 'Content-Type: application/json' \
--data-raw '{
	“userFirstName”: “Axel”,
  “userLastName”: “Slabos”,
  “email”: “template.email@gmail. com”,
  “password”: “template_password”
}'
```

#### Response:
HTTP status code: 200

```
{
    "parameterName": "_csrf",
    "headerName": "X-CSRF-TOKEN",
    "token": "cabef633-3b34-45db-801f-d5b21b9e7bee"
}
```

### GET /login
Authorization

#### Request body:
```
{
	“email”:          string,
	“password”:       string
}
```

#### Example:

```
curl --location --request POST 'https://cub.it/login' \
--header 'Content-Type: application/json' \
--data-raw '{
  “email”: “template.email@gmail. com”,
  “password”: “template_password”
}'
```

#### Response:
HTTP status code: 200

```
{
    "parameterName": "_csrf",
    "headerName": "X-CSRF-TOKEN",
    "token": "cabef633-3b34-45db-801f-d5b21b9e7bee"
}
```
