# CRUD operations

The JSON-RPC API can be used to perform multiple [*CRUD* (Create, Read, Update, Delete)](<https://en.wikipedia.org/wiki/Create,_read,_update_and_delete>) on an instance.

## Create

### Request params

To create a record inside a new model, the `create` method argument is used.

In this example, a new contact and it's address are created in the `res.partner` model.

| Arguments  | Field Type | Description                                  | Required | Value       |
|------------|------------|----------------------------------------------|----------|-------------|
| `database` | `string`   | Database name                                | True     |             |
| `userID`   | `integer`  | The user ID returned in the<br>login request | True     |             |
| `passwd`   | `string`   | The user password                            | True     |             |
| `model`    | `string`   | Model to act on                              | True     | res.partner |
| `method`   | `string`   | Operation method                             | True     | create      |

```json
"service": "object",
"method": "execute",
"args": [
    "database",
    userID,
    "passwd",
    "res.partner",
    "create",
    {
        "name": "Konvergo",
        "street": "407 McGill St",
        "street2": "Suite 501",
        "city": "Montreal",
        "state_id": 543,
        "zip": "H2Y 2G3",
        "country_id": 38
    }
]
```

### Response body

```json
{
  "id": null,
  "jsonrpc": "2.0",
  "result": 45
}
```

The field `result` contains the newly created record ID as an integer.

## Read

### Request params

To read a record, the `read` method argument is used.

In this example, a contact and it's address are fetched from the `res.partner` model by using the contact ID.

| Arguments  | Field Type | Description                                  | Required | Value       |
|------------|------------|----------------------------------------------|----------|-------------|
| `database` | `string`   | Database name                                | True     |             |
| `userID`   | `integer`  | The user ID returned in the<br>login request | True     |             |
| `passwd`   | `string`   | The user password                            | True     |             |
| `model`    | `string`   | Model to act on                              | True     | res.partner |
| `method`   | `string`   | Operation method                             | True     | read        |

```json
"service": "object",
"method": "execute",
"args": [
    "database",
    userID,
    "passwd",
    "res.partner",
    "read",
    [
        45
    ],
    [
        "name",
        "street",
        "street2",
        "city",
        "state_id",
        "zip",
        "country_id"
    ]
]
```

### Response body

```json
{
  "id": null,
  "jsonrpc": "2.0",
  "result": [
    {
      "country_id": [
        38,
        "Canada"
      ],
      "street2": "Suite 501",
      "name": "Konvergo",
      "zip": "H2Y 2G3",
      "id": 45,
      "street": "407 McGill St",
      "state_id": [
        543,
        "Quebec (CA)"
      ],
      "city": "Montreal"
    }
  ]
}
```

The field `result` contains the newly created record ID as an integer.
