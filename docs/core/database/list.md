# Odoo List Database

List the server's databases using the `list` method of the `db` service.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "list",
    "args": [
    ]
  }
}
```

## Request

List all the databases in a server.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "db",
    "method": "list",
    "args": [
    ]
  }
}
```

### Response

``` json title="Response body"
{
  "jsonrpc": "2.0",
  "id": null,
  "result": [
    "prod",
    "test"
  ]
}
```
