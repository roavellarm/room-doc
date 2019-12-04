[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Feedback

## Feedback

A feedback is an information about reactions to a product that is used as a basis for improvement.

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **email** | _string_ | the email of the user that sends the feedback | `"example"` |
| **id** | _integer_ | unique identifier of the feedback | `42` |
| **name** | _string_ | the name of the user that sends the feedback | `"example"` |
| **negatives** | _string_ | the negatives feedback from the user | `"example"` |
| **positives** | _string_ | the positives feedback from the user | `"example"` |

## Feedback Create

Create a new feedback

```text
POST /feedback
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **email** | _string_ | the email of the user that sends the feedback | `"example"` |
| **id** | _integer_ | unique identifier of the feedback | `42` |
| **name** | _string_ | the name of the user that sends the feedback | `"example"` |
| **negatives** | _string_ | the negatives feedback from the user | `"example"` |
| **positives** | _string_ | the positives feedback from the user | `"example"` |

### Curl Example

```bash
$ curl -n -X POST https://production-room-api.herokuapp.com/feedback \
  -d '{
  "id": 42,
  "name": "example",
  "email": "example",
  "positives": "example",
  "negatives": "example"
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

