# Odoo Dump Database

!!! danger
    The super administrator password of the database manager is required to perform this operation.

Backups a database using the `dump` method the `db` service. Returns the dump as the *`format`* specified containing the SQL dump. If there is a filestore directory, it will be included in the result.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "dump",
    "args": [
      "password",
      "db",
      "format"
    ]
  }
}
```

## Request

Dump the *`db`* database.

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
      "base64"
    ]
  }
}
```

### Response

``` json title="Response body"
{
  "jsonrpc": "2.0",
  "id": null,
  "result": "UEdETVABDgAECAEBAQA..."
}
```
