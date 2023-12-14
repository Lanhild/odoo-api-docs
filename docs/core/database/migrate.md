# Odoo Migrate Database

!!! danger
    The super administrator password of the database manager is required to perform this operation.

Migrates the *`db`* databases list by updating the base module using the `migrate_database` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "migrate_database",
    "args": [
      "password",
      [
        "db"
      ]
    ]
  }
}
```

## Request

Migrates the *`prod`* and *`test`* database.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "migrate_database",
    "args": [
      "super_admin_passwd",
      [
        "prod",
        "test"
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
