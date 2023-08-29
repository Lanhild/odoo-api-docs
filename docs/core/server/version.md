# Odoo Server Version

Retrieves the server version info using the `version` method of the `common` method.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "common",
    "method": "version",
    "args": [
    ]
  }
}
```

## Request

Retrieve the server version info.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "common",
    "method": "version",
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
  "result": {
    "server_version_info": [
      12,
      0,
      0,
      "final",
      0,
      ""
    ],
    "server_serie": "12.0",
    "server_version": "12.0-20211006",
    "protocol_version": 1
  }
}
```
