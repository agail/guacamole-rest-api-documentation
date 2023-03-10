<!-- omit in toc -->
# Users

Manage users.

<!-- omit in toc -->
# Table of Contents

- [List Users](#list-users)
    - [Headers](#headers)
    - [Path Parameters](#path-parameters)
    - [Query Parameters](#query-parameters)
    - [Request Body](#request-body)
  - [Response](#response)
    - [Status Code](#status-code)
    - [Response Body](#response-body)
- [Details of User](#details-of-user)
    - [Headers](#headers-1)
    - [Path Parameters](#path-parameters-1)
    - [Query Parameters](#query-parameters-1)
    - [Request Body](#request-body-1)
  - [Response](#response-1)
    - [Status Code](#status-code-1)
    - [Response Body](#response-body-1)
- [Details of Self](#details-of-self)
    - [Headers](#headers-2)
    - [Path Parameters](#path-parameters-2)
    - [Query Parameters](#query-parameters-2)
    - [Request Body](#request-body-2)
  - [Response](#response-2)
    - [Status Code](#status-code-2)
    - [Response Body](#response-body-2)
- [Details of User Permissions](#details-of-user-permissions)
    - [Headers](#headers-3)
    - [Path Parameters](#path-parameters-3)
    - [Query Parameters](#query-parameters-3)
    - [Request Body](#request-body-3)
  - [Response](#response-3)
    - [Status Code](#status-code-3)
    - [Response Body](#response-body-3)
- [Details of User Effective Permissions](#details-of-user-effective-permissions)
    - [Headers](#headers-4)
    - [Path Parameters](#path-parameters-4)
    - [Query Parameters](#query-parameters-4)
    - [Request Body](#request-body-4)
  - [Response](#response-4)
    - [Status Code](#status-code-4)
    - [Response Body](#response-body-4)
- [Details of User Groups](#details-of-user-groups)
    - [Headers](#headers-5)
    - [Path Parameters](#path-parameters-5)
    - [Query Parameters](#query-parameters-5)
    - [Request Body](#request-body-5)
  - [Response](#response-5)
    - [Status Code](#status-code-5)
    - [Response Body](#response-body-5)
- [Details of User History](#details-of-user-history)
    - [Headers](#headers-6)
    - [Path Parameters](#path-parameters-6)
    - [Query Parameters](#query-parameters-6)
    - [Request Body](#request-body-6)
  - [Response](#response-6)
    - [Status Code](#status-code-6)
    - [Response Body](#response-body-6)
- [Assign User to User Groups](#assign-user-to-user-groups)
    - [Headers](#headers-7)
    - [Path Parameters](#path-parameters-7)
    - [Query Parameters](#query-parameters-7)
    - [Request Body](#request-body-7)
  - [Response](#response-7)
    - [Status Code](#status-code-7)
    - [Response Body](#response-body-7)
- [Revoke User from User Groups](#revoke-user-from-user-groups)
    - [Headers](#headers-8)
    - [Path Parameters](#path-parameters-8)
    - [Query Parameters](#query-parameters-8)
    - [Request Body](#request-body-8)
  - [Response](#response-8)
    - [Status Code](#status-code-8)
    - [Response Body](#response-body-8)
- [Assign User to Connections](#assign-user-to-connections)
    - [Headers](#headers-9)
    - [Path Parameters](#path-parameters-9)
    - [Query Parameters](#query-parameters-9)
    - [Request Body](#request-body-9)
  - [Response](#response-9)
    - [Status Code](#status-code-9)
    - [Response Body](#response-body-9)
- [Revoke User from Connections](#revoke-user-from-connections)
    - [Headers](#headers-10)
    - [Path Parameters](#path-parameters-10)
    - [Query Parameters](#query-parameters-10)
    - [Request Body](#request-body-10)
  - [Response](#response-10)
    - [Status Code](#status-code-10)
    - [Response Body](#response-body-10)
- [Update User Password](#update-user-password)
    - [Headers](#headers-11)
    - [Path Parameters](#path-parameters-11)
    - [Query Parameters](#query-parameters-11)
    - [Request Body](#request-body-11)
  - [Response](#response-11)
    - [Status Code](#status-code-11)
    - [Response Body](#response-body-11)
- [Update User](#update-user)
    - [Headers](#headers-12)
    - [Path Parameters](#path-parameters-12)
    - [Query Parameters](#query-parameters-12)
    - [Request Body](#request-body-12)
  - [Response](#response-12)
    - [Status Code](#status-code-12)
    - [Response Body](#response-body-12)
- [Create User](#create-user)
    - [Headers](#headers-13)
    - [Path Parameters](#path-parameters-13)
    - [Query Parameters](#query-parameters-13)
    - [Request Body](#request-body-13)
  - [Response](#response-13)
    - [Status Code](#status-code-13)
    - [Response Body](#response-body-13)
- [Delete User](#delete-user)
    - [Headers](#headers-14)
    - [Path Parameters](#path-parameters-14)
    - [Query Parameters](#query-parameters-14)
    - [Request Body](#request-body-14)
  - [Response](#response-14)
    - [Status Code](#status-code-14)
    - [Response Body](#response-body-14)

## List Users

List users.

<!-- omit in toc -->
### GET /api/session/data/{{data_source}}/users

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source

#### Query Parameters

- token (string, required) - Auth token

#### Request Body

None.

### Response

#### Status Code

- 200 - OK

#### Response Body Example

```json
{
  "guacadmin": {
    "username": "guacadmin",
    "attributes": {
      "guac-email-address": null,
      "guac-organizational-role": null,
      "guac-full-name": null,
      "expired": null,
      "timezone": null,
      "access-window-start": null,
      "guac-organization": null,
      "access-window-end": null,
      "disabled": null,
      "valid-until": null,
      "valid-from": null
    },
  "someuser": {
    "username": "someuser",
    "attributes": {
      "guac-email-address": "some.user@company.local",
      "guac-organizational-role": "user",
      "guac-full-name": "Some User",
      "expired": null,
      "timezone": null,
      "access-window-start": null,
      "guac-organization": null,
      "access-window-end": null,
      "disabled": null,
      "valid-until": null,
      "valid-from": null
    }
  }
}
```

---

## Details of User

Details of user.

<!-- omit in toc -->
### GET /api/session/data/{{data_source}}/users/{{username}}

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

None.

### Response

#### Status Code

- 200 - OK

#### Response Body Example

```json
{
  "username": "someuser",
  "attributes": {
    "guac-email-address": "some.user@company.local",
    "guac-organizational-role": "user",
    "guac-full-name": "Some User",
    "expired": null,
    "timezone": null,
    "access-window-start": null,
    "guac-organization": null,
    "access-window-end": null,
    "disabled": null,
    "valid-until": null,
    "valid-from": null
  }
}
```

---

## Details of Self

Details of token owner.

<!-- omit in toc -->
### GET /api/session/data/{{data_source}}/self

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source

#### Query Parameters

- token (string, required) - Auth token

#### Request Body

None.

### Response

#### Status Code

- 200 - OK

#### Response Body Example

```json
{
  "username": "guacadmin",
  "attributes": {
    "guac-email-address": null,
    "guac-organizational-role": null,
    "guac-full-name": null,
    "guac-organization": null
  },
  "lastActive": 1678440189434
}
```

---

## Details of User Permissions

Details of user permissions.

<!-- omit in toc -->
### GET /api/session/data/{{data_source}}/users/{{username}}/permissions

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

None.

### Response

#### Status Code

- 200 - OK

#### Response Body Example

```json
{
  "connectionPermissions": {},
  "connectionGroupPermissions": {},
  "sharingProfilePermissions": {},
  "activeConnectionPermissions": {},
  "userPermissions": {
    "someuser": [
      "READ"
    ]
  },
  "userGroupPermissions": {},
  "systemPermissions": []
}
```

---

## Details of User Effective Permissions

Details of user effective permissions.

<!-- omit in toc -->
### GET /api/session/data/{{data_source}}/users/{{username}}/effectivePermissions

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

None.

### Response

#### Status Code

- 200 - OK

#### Response Body Example

```json
{
  "connectionPermissions": {
    "3": [
      "READ"
    ],
    "5": [
      "READ"
    ]
  },
  "connectionGroupPermissions": {
    "2": [
      "READ"
    ]
  },
  "sharingProfilePermissions": {},
  "activeConnectionPermissions": {},
  "userPermissions": {
    "admin": [
      "READ",
      "UPDATE"
    ]
  },
  "userGroupPermissions": {},
  "systemPermissions": [
    "CREATE_USER",
    "CREATE_USER_GROUP",
    "CREATE_CONNECTION",
    "CREATE_CONNECTION_GROUP",
    "CREATE_SHARING_PROFILE",
    "ADMINISTER"
  ]
}
```

---

## Details of User Groups

Details of user groups.

<!-- omit in toc -->
### GET /api/session/data/{{data_source}}/users/{{username}}/userGroups

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

None.

### Response

#### Status Code

- 200 - OK

#### Response Body

**@TODO**

---

## Details of User History

Details of user history.

<!-- omit in toc -->
### GET /api/session/data/{{data_source}}/users/{{username}}/history

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

None.

### Response

#### Status Code

- 200 - OK

#### Response Body

**@TODO**

---

## Assign User to User Groups

Assign user to user groups.

<!-- omit in toc -->
### PATCH /api/session/data/{{data_source}}/users/{{username}}/userGroups

#### Headers

- Content-Type (string, required) - application/json

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

Body must be [json-patch](http://jsonpatch.com/) format.

```json
[
  {
    "op": "add",
    "path": "/",
    "value": "{{user_group}}"
  }
]
```

### Response

#### Status Code

- 204 - No Content

#### Response Body

This request does not return a response body.

---

## Revoke User from User Groups

Revoke user from user groups.

<!-- omit in toc -->
### PATCH /api/session/data/{{data_source}}/users/{{username}}/userGroups

#### Headers

- Content-Type (string, required) - application/json

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

Body must be [json-patch](http://jsonpatch.com/) format.

```json
[
  {
    "op": "remove",
    "path": "/",
    "value": "{{user_group}}"
  }
]
```

### Response

#### Status Code

- 204 - No Content

#### Response Body

This request does not return a response body.

---

## Assign User to Connections

Assign user to connections.

<!-- omit in toc -->
### PATCH /api/session/data/{{data_source}}/users/{{username}}/permissions

#### Headers

- Content-Type (string, required) - application/json

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

Body must be [json-patch](http://jsonpatch.com/) format.

```json
[
  {
    "op": "add",
    "path": "/connectionPermissions/{{connectionId}}",
    "value": "READ"
  }
]
```

You may also include connection groups (folders), and must if the connection that you wish to allow access to is within a connection group.

```json
[
  {
    "op": "add",
    "path": "/connectionGroupPermissions/{{connectionGroupId}}",
    "value": "READ"
  }
]
```


### Response

#### Status Code

- 204 - No Content

#### Response Body

This request does not return a response body.

---

## Revoke User from Connections

Revoke user from connections.

<!-- omit in toc -->
### PATCH /api/session/data/{{data_source}}/users/{{username}}/permissions

#### Headers

- Content-Type (string, required) - application/json

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

Body must be [json-patch](http://jsonpatch.com/) format.

```json
[
  {
    "op": "remove",
    "path": "/connectionPermissions/{{connectionId}}",
    "value": "READ"
  }
]
```

You may also include connection groups (folders)

```json
[
  {
    "op": "remove",
    "path": "/connectionGroupPermissions/{{connectionGroupId}}",
    "value": "READ"
  }
]
```

### Response

#### Status Code

- 204 - No Content

#### Response Body

This request does not return a response body.

---

## Update User Password

Updates user password.

<!-- omit in toc -->
### PUT /api/session/data/{{data_source}}/users/{{username}}/password

#### Headers

- Content-Type (string, required) - application/json

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

- oldPassword (string, required) - Old password
- newPassword (string, required) - New password

```json
{
  "oldPassword": "{{oldPassword}}",
  "newPassword": "{{newPassword}}"
}
```

### Response

#### Status Code

- 204 - No Content

#### Response Body

This request does not return a response body.

---

## Update User

Updates user.

<!-- omit in toc -->
### PUT /api/session/data/{{data_source}}/users/{{username}}

#### Headers

- Content-Type (string, required) - application/json

#### Path Parameters

- data_source (string, required) - Data source
- username (string, required) - Username

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

**@TODO**

```json
{
  "username": "{{username}}",
  "attributes": {
    "guac-email-address": null,
    "guac-organizational-role": null,
    "guac-full-name": null,
    "expired": "",
    "timezone": null,
    "access-window-start": "",
    "guac-organization": null,
    "access-window-end": "",
    "disabled": "",
    "valid-until": "",
    "valid-from": ""
  }
}
```

### Response

#### Status Code

- 204 - No Content

#### Response Body

This request does not return a response body.

---

## Create User

Creates a user.

<!-- omit in toc -->
### POST /api/session/data/{{data_source}}/users

#### Headers

- Content-Type (string, required) - application/json

#### Path Parameters

- data_source (string, required) - Data source

#### Query Parameters

- token (string, required) - Auth Token

#### Request Body

**@TODO**

```json
{
  "username": "test",
  "password": "pass",
  "attributes": {
    "disabled": "",
    "expired": "",
    "access-window-start": "",
    "access-window-end": "",
    "valid-from": "",
    "valid-until": "",
    "timezone": null,
    "guac-full-name": "",
    "guac-organization": "",
    "guac-organizational-role": ""
  }
}
```

### Response

#### Status Code

- 200 - OK

#### Response Body

**@TODO**

## Delete User

Delete user.

<!-- omit in toc -->
### DELETE /api/session/data/{{data_source}}/users/{{username}}

#### Headers

None.

#### Path Parameters

- data_source (string, required) - Data source
- username (integer, required) - Username

#### Query Parameters

- token (string, required) - Auth token

#### Request Body

None.

### Response

#### Status Code

- 204 - No Content

#### Response Body

This request does not return a response body.

---

[Back to Top](#users)
