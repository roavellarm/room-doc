[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Social Media

## Social Media

A Login with Social Media

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| [**email**](social_media.md#resource-user) | _email_ | the email of the user | `"username@example.com"` |
| [**first\_name**](social_media.md#resource-user) | _string_ | first name of the user | `"example"` |
| [**id**](social_media.md#resource-user) | _integer_ | unique identifier of the user | `42` |
| [**image**](social_media.md#resource-user) | _nullable string_ | the image of the user | `null` |
| [**last\_name**](social_media.md#resource-user) | _string_ | last name of the user | `"example"` |
| [**mood**](social_media.md#resource-user) | _nullable object_ | the current user mood | `null` |

## Social Media Create

create a new Login with social media

```text
POST /auth/social_media/{social_media_provider}
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **access\_token** | _nullable string_ | google generated access\_token | `null` |
| **email** | _nullable email_ | the email of the user | `null` |
| **family\_name** | _nullable string_ | last name of the user | `null` |
| **given\_name** | _nullable string_ | first name of the user | `null` |
| **input\_token** | _nullable string_ | facebook input token | `null` |
| **name** | _nullable string_ | name that comes from facebook | `null` |
| **token\_id** | _nullable string_ | token id built for an order | `null` |

### Curl Example

```bash
$ curl -n -X POST https://production-room-api.herokuapp.com/auth/social_media/$SOCIAL_MEDIA_PROVIDER \
  -d '{
  "email": "username@example.com",
  "given_name": "example",
  "family_name": "example",
  "token_id": "example",
  "input_token": "example",
  "name": "example",
  "access_token": "example"
}' \
  -H "Content-Type: application/json"
```

### Response Example

```text
HTTP/1.1 201 Created
```

```javascript
null
```

