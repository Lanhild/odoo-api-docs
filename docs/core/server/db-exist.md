# Odoo Database Existence

Checking if a database exists can be done using the `db_exist` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "db_exist",
    "args": [
      "db"
    ]
  }
}
```

## Request

Checks if the *`db`* database exists in this server.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "db_exist",
    "args": [
        "prod"
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
