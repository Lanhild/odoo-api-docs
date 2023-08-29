# Odoo Drop Database

!!! danger
    The super administrator password of the database manager is required to perform this operation.

Drop[^1] a database using the `drop` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "drop",
    "args": [
      "password",
      "db"
    ]
  }
}
```

## Request

Drop the *`db`* database.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "drop",
    "args": [
      "super_admin_passwd",
      "prod_copy"
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

[^1]: Delete the database and all the physical disk files used by the database.
