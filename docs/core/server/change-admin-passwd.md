# Odoo Change Admin Password

!!! danger
    The super administrator password of the database manager is required to perform this operation.

The database manager master password can be changed using the `change_admin_password` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "change_admin_password",
    "args": [
      "password",
      "new_password"
    ]
  }
}
```

## Request

Change the database manager master password from *`password`* to *`new_password`*.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "change_admin_password",
    "args": [
      "super_admin_password",
      "an_even_better_password"
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
