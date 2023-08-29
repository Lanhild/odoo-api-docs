# Odoo Delete Record

Deleting a record can be done using the `unlink` argument method of the `object` service.

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
      "unlink",
      [
        id
      ]
    ]
  }
}
```

## Request

Deletes an existing record with the id *`id`* in the model *`model`*.

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
      "unlink",
      [
        7
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
  "result": true
}
```
