# Important information to get started

## Prerequisites

In order to achieve a connection with a database, you need the following:

- An instance URI - for example; `https://odoo.example.com`
- An available database
- A valid user email and password combination

This API only has one endpoint `/jsonrpc`.

## Common request payload

Odoo's ORM API operates using a particular format; it follows the [*JSON-RPC 2.0 Specification*](https://www.jsonrpc.org/specification).

Thus, some of the parameters and values used inside the request payload an API call are redundant. Here are some of them:

| Field Name | Field Type | Required | Description                                                | Value         |
|------------|------------|----------|------------------------------------------------------------|---------------|
| `jsonrpc`  | `string`   | True     | Specifies the JSON-RPC definition<br>version.              | 2.0           |
| `method`   | `string`   | True     | Method to execute                                          | call          |
| `params`   | `Object`   | True     | Contains all of the parameters<br>specific to this request | Object object |

## Definition

Throughout this entire API reference, some of those parameters will have example values - *for the sake of documentation* - and others will have prefixed values that must be respected.

All of the non-mandatory values will be thoroughly described and highlighted at the beginning of a section using a table.

## Notice

Please note that the examples are formatted without the redundant parameters described in [the table just above](#common-request-payload) but only the `params` object values, like the following:

```diff
-{
-  "jsonrpc": "2.0",
-  "method": "call",
-  "params": {
+    "service": "common",
+    "method": "login",
+    "args": [
+      "database",
+      "your.user@example.com",
+      "passwd"
+    ]
-  }
-}
```

In the case you might need to refresh your memory about a classic payload syntax, [refer to the current page](#).
