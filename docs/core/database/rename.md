# Odoo Rename Database

!!! danger
    The super administrator password of the database manager is required to perform this operation.

Renames the *`db`* database to *`new_db_name`* using the `rename` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "rename",
    "args": [
      "password",
      "db",
      "dump_file"
    ]
  }
}
```

## Request

Restore the *`prod`* database.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "dump",
    "args": [
      "super_admin_passwd",
      "prod",
      "prod_super"
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
