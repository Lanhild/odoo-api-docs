# Odoo Update Record

Updating a record can be done using the `update` argument method of the `object` service.

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
      "update",
      [
        id
      ],
      {
        "field": "value"
      }
    ]
  }
}
```

## Request

Updates the record with the ID *`id`* in the model *`model`* with the field(s) *`field`* of a value of *`value`*.

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
      "update",
      [
        9
      ],
      {
        "name": "Corp & Co.",
        "email": "corp.co@example.com"
      }
    ]
  }
}
```

### Response

``` json title="Response body"
{
  "jsonrpc": "2.0",
  "id": null
}
```
