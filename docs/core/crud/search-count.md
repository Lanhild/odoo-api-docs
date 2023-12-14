# Count Records

Similar to the `search_read` method, the `search_count` method can be used to directly compute the number of records corresponding to the search criteria.

``` json title="Method"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "object",
    "method": "execute",
    "args": [
      "db",
      uid,
      "password",
      "model",
      "search_count",
      [
        [
        "field",
        operator,
        "value"
        ]
      ]
    ]
  }
}
```

## Request

Searches for records with the field *`field`* to compare with the value *`value`* using the operator *`operator`*. Returns the number of records matching the search criteria.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "object",
    "method": "execute",
    "args": [
      "prod",
      1,
      "super_secret_password",
      "res.partner",
      "search_count",
      [
        [
          "is_company",
          "!=",
          true
        ]
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
  "result": 2000
}
```
