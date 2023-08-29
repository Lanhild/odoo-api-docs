# Odoo Duplicate Database

!!! danger
    The super administrator password of the database manager is required to perform this operation.

Duplicate an existing database using the `duplicate_database` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "duplicate_database",
    "args": [
      "password",
      "origin_db",
      "new_db"
    ]
  }
}
```

## Request

Duplicate the exisiting *`origin_db`* into the new *`new_db`*.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "duplicate_database",
    "args": [
      "super_admin_passwd",
      "prod",
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
