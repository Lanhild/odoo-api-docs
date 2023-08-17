# Login to a given database

## Request parameters

In order to login to an Odoo instance, the following params should be used

| Field Name | Field Type | Description                                            | Required | Value         |
|------------|------------|--------------------------------------------------------|----------|---------------|
| `service`  | `string`   | Service to act on.                                     | True     | common        |
| `method`   | `string`   | Method to execute                                      | True     | login         |
| `args`     | `Object`   | Contains all of the<br>arguments related to the method | True     | Object object |

```json
"service": "common",
"method": "login",
"args": [
  "<database>",
  "<your.user@example.com>",
  "<passwd>"
]
```

## Response body

```json
{
  "id": null,
  "jsonrpc": "2.0",
  "result": 1
}
```

The field `result` contains the UID of the email used as a parameter.

This integer can then be used to authenticate requests made to an instance.
