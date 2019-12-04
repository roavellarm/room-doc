[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# User

## User

A user

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **email** | _email_ | the email of the user | `"username@example.com"` |
| **first\_name** | _string_ | first name of the user | `"example"` |
| **id** | _integer_ | unique identifier of the user | `42` |
| **image** | _nullable string_ | the image of the user | `null` |
| **last\_name** | _string_ | last name of the user | `"example"` |
| **mood** | _nullable object_ | the current user mood | `null` |

## User List

List all users

```text
GET /user
```

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/user
 -G \
  -d
```

### Response Example

```text
HTTP/1.1 200 OK
```

```javascript
null
```

## User Info

Is shows the info for existing user.

```text
GET /user/{user_id}
```

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/user/$USER_ID
 -G \
  -d
```

### Response Example

```text
HTTP/1.1 200 OK
```

```javascript
null
```

## User Update

Update the user info

```text
PUT /user/{user_id}
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **email** | _email_ | the email of the user | `"username@example.com"` |
| **first\_name** | _string_ | first name of the user | `"example"` |
| **image** | _nullable string_ | the image of the user | `null` |
| **last\_name** | _string_ | last name of the user | `"example"` |
| **mood** | _nullable string_ | the mood of the user | `null` |

### Curl Example

```bash
$ curl -n -X PUT https://production-room-api.herokuapp.com/user/$USER_ID \
  -d '{
  "first_name": "example",
  "last_name": "example",
  "email": "username@example.com",
  "image": null,
  "mood": null
}' \
  -H "Content-Type: application/json"
```

### Response Example

```text
HTTP/1.1 200 OK
```

```javascript
null
```

## User Leave rooms

It takes out the user all rooms

```text
PUT /user/{user_id}/leave_rooms
```

### Curl Example

```bash
$ curl -n -X PUT https://production-room-api.herokuapp.com/user/$USER_ID/leave_rooms \
  -d '{
}' \
  -H "Content-Type: application/json"
```

### Response Example

```text
HTTP/1.1 200 OK
```

```javascript
null
```

