# Odoo Restore Database

!!! danger
    The super administrator password of the database manager is required to perform this operation.

Restores the *`dump_file`* database into the new *`db`* database using the `restore` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "restore",
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
      "prod_restored",
      "UEdETVABDgAECAEBAQA..."
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
