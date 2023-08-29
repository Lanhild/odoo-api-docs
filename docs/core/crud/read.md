# Odoo Read Record

Reading a specific record can be done using the `read` argument method of the `object` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "object",
    "method": "execute",
    "args": [
      "db",
      uid,
      "password",
      "model",
      "read",
      [
        id
      ],
      [
        "fields"
      ]
    ]
  }
}
```

## Request

Reads a record with the ID *`id`* in the model *`model`* and returns the data with the list of fields in the *`fields`* array.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "object",
    "method": "execute",
    "args": [
      "prod",
      1,
      "super_secret_password",
      "res.partner",
      "read",
      [
        6
      ],
      [
        "name",
        "email",
        "phone"
      ]
    ]
  }
}
```

### Response

``` json title="Response body"
{
  "jsonrpc": "2.0",
  "id": null,
  "result": [
    {
      "id": 3,
      "name": "Administrator",
      "email": "admin@example.com",
      "phone": "12345678900"
    }
  ]
}
```
