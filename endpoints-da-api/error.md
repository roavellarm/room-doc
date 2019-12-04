[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Error

## Error

An error represents a failed action in the API

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **id** | _string_ | unique identifier of error  **pattern:** `^\w+$` | `"example"` |
| **message** | _string_ | message of error | `"example"` |

## Error Info

Info for existing error.

```text
GET /errors/{error_id}
```

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/errors/$ERROR_ID
```

### Response Example

```text
HTTP/1.1 200 OK
```

```javascript
{
  "id": "example",
  "message": "example"
}
```

