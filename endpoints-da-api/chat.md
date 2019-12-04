[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Chat

## Chat

An chat is a virtual space to talk about something with someone.

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **created\_at** | _date-time_ | the message creation date and time | `"2015-01-01T12:00:00Z"` |
| **id** | _integer_ | unique identifier of the chat | `42` |
| **message** | _string_ | the message that the user is sending | `"example"` |
| **room\_id** | _integer_ | the id of the room that the chat belongs to | `42` |
| **user\_id** | _integer_ | the id of the user that is sending a message through the chat | `42` |

## Chat Info

Info for existing chat.

```text
GET /chat/{chat_id}
```

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/chat/$CHAT_ID
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

## Chat Create

Create a new chat message

```text
POST /chat
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **message** | _string_ | the message that the user is sending | `"example"` |
| **room\_id** | _integer_ | unique identifier of the room | `42` |

### Curl Example

```bash
$ curl -n -X POST https://production-room-api.herokuapp.com/chat \
  -d '{
  "room_id": 42,
  "message": "example"
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

