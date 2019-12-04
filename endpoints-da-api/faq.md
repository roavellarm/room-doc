[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Faq

## Faq

A faq is a series of frequently asked questions paired with answers that provides basic information

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **answer** | _string_ | an answer of a question of the faq | `"example"` |
| **id** | _integer_ | unique identifier of the faq | `42` |
| **question** | _string_ | a question of the faq | `"example"` |

## Faq List

List all faqs, that is, all faq questions and answers

```text
GET /faq
```

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/faq
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

