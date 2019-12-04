[<- Voltar ao menu](/README.md#artefatos-do-projeto)


# Org

## Org

An org is an entity such as a company or organization.

## Attributes

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **description** | _nullable string_ | a description of the org | `null` |
| **id** | _integer_ | unique identifier of the org | `42` |
| **image** | _nullable string_ | an image such as an logo of the org | `null` |
| **members** | _nullable array_ | the members list of the org | `null` |
| **name** | _string_ | the name of the org | `"example"` |
| **rooms** | _nullable array_ | the rooms list of the org | `null` |
| **user\_id** | _integer_ | the id of the user that created the org | `42` |

## Org List

List of all the current user orgs

```text
GET /org
```

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/org
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

## Org Create

Create a new org

```text
POST /org
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **description** | _nullable string_ | a description of the org | `null` |
| **id** | _integer_ | unique identifier of the org | `42` |
| **image** | _nullable string_ | an image such as an logo of the org | `null` |
| **name** | _string_ | the name of the org | `"example"` |
| **user\_id** | _integer_ | the id of the user that created the org | `42` |

### Curl Example

```bash
$ curl -n -X POST https://production-room-api.herokuapp.com/org \
  -d '{
  "id": 42,
  "user_id": 42,
  "name": "example",
  "description": null,
  "image": null
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

## Org Info

Info for existing org.

```text
GET /org/{org_id}
```

### Curl Example

```bash
$ curl -n https://production-room-api.herokuapp.com/org/$ORG_ID
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

## Org Add member

It adds the user as a member of the organization

```text
PUT /org/{org_id}/add_member
```

### Optional Parameters

| Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| **email** | _email_ | the email of the user | `"username@example.com"` |
| **id** | _integer_ | unique identifier of the org | `42` |

### Curl Example

```bash
$ curl -n -X PUT https://production-room-api.herokuapp.com/org/$ORG_ID/add_member \
  -d '{
  "id": 42,
  "email": "username@example.com"
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

