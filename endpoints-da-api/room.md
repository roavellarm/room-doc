[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Room

## Room

An room is virtual place to communicate in an org.

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **avatar\_image** | _nullable string_ | an avatar image of the room | `null` |
| **background\_image** | _nullable string_ | a background image of the room | `null` |
| **id** | _integer_ | unique identifier of the room | `42` |
| **online\_members** | _nullable array_ | the list of users that are online in the specific room | `null` |
| **org\_id** | _integer_ | the id of the org that the rooms belongs to | `42` |
| **subtitle** | _nullable string_ | the subtitle of the room | `null` |
| **title** | _string_ | the title of the room | `"example"` |
| **token** | _nullable string_ | a token of the room used for audio and video calls | `null` |

## Room Create

Create a new room

```text
POST /room
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **avatar\_image** | _nullable string_ | an avatar image of the room | `null` |
| **background\_image** | _nullable string_ | a background image of the room | `null` |
| **id** | _integer_ | unique identifier of the room | `42` |
| **org\_id** | _integer_ | the id of the org that the rooms belongs to | `42` |
| **subtitle** | _nullable string_ | the subtitle of the room | `null` |
| **title** | _string_ | the title of the room | `"example"` |

### Curl Example

```bash
$ curl -n -X POST https://production-room-api.herokuapp.com/room \
  -d '{
  "id": 42,
  "org_id": 42,
  "title": "example",
  "subtitle": null,
  "background_image": null,
  "avatar_image": null
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

## Room Room access

It updates the current room that the user is in

```text
PUT /room_access
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **id** | _integer_ | unique identifier of the room | `42` |

### Curl Example

```bash
$ curl -n -X PUT https://production-room-api.herokuapp.com/room_access \
  -d '{
  "id": 42
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

