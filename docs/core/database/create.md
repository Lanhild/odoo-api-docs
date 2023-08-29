# Odoo Create Database

!!! danger
    The super administrator password of the database manager is required to perform this operation.

A new database can be created using the `create_database` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "create_database",
    "args": [
      "password",
      "db",
      demo,
      "lang",
      "password"
    ]
  }
}
```

## Request

This request creates a new database name *`db`* with *`password`* as the administrator password and localized using the *`lang`* parameter. The *`demo`* flag has to be set to `true` if the database should be populated with demo data.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "create_database",
    "args": [
      "super_admin_passwd",
      "prod",
      false,
      "fr_CA",
      "my_admin_passwd"
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
