[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Admin texts

## Admin Texts

An admin text is a text for an admin area

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **id** | _integer_ | unique identifier of the Admin Text | `42` |

## Admin Texts List

Show the admin texts for the tags.

```text
GET /admin_texts
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **tags** | _array_ |  | `[null]` |

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/admin_texts
 -G \
  -d tags[]=
```

### Response Example

```text
HTTP/1.1 200 OK
```

```javascript
null
```

