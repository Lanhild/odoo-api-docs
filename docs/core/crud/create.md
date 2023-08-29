# Odoo Create Record

Creating a record can be done using the `create` argument method of the `object` service.

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
      "create",
      {
        "field": "value"
      }
    ]
  }
}
```

## Request

Creates a new record in the model *`model`* using the values *`field`* and *`value`*.

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
      "create",
      {
        "name": "Super Cool Company",
        "email": "super.cool@company.com",
        "phone": "12345678900"
      }
    ]
  }
}
```

### Response

``` json title="Response body"
{
  "jsonrpc": "2.0",
  "id": null,
  "result": 7
}
```
