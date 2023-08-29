# Odoo Search Records

Searching for records can be done using the `search_read` argument method of the `object` service.

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
      "search_read",
      [
        [
        "field",
        operator,
        "value"
        ]
      ],
      [
        "fields"
      ]
    ]
  }
}
```

## Request

Searches for records with the field *`field`* to compare with the value *`value`* using the operator *`operator`*. Returns the data with the list of fields in the *`fields`* array.

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
      "search_read",
      [
        [
        "country_id",
        "=",
        38
        ]
      ],
      [
        "name",
        "country_id"
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
  "result": [
    {
      "id": 9,
      "name": "Another Corp",
      "country_id": [
        38,
        "Canada"
      ]
    },
    {
      "id": 1,
      "name": "My Company",
      "country_id": [
        38,
        "Canada"
      ]
    },
    {
      "id": 8,
      "name": "Super Cool Company",
      "country_id": [
        38,
        "Canada"
      ]
    }
  ]
}
```
