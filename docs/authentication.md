# Authentication

The Odoo JSON-RPC API uses an UID and password[^1] combination to authenticate requests. You can find your own UID by executing the following request.

!!! warning

    Since your API access holds the same permissions as the one you have on the web interface, be sure to keep your credentials secure. Never share a password in publicly accessible areas such as GitHub, client-side code or even paper notes "hidden" under a keyboard.

Authentication to the API is performed using your user login and password[^2].

All API requests made using an invalid format will systematically fail or render into an error.

## Odoo Server Authentication

Logging into a database can be done using the `login` method of the `common` service.
  
``` json title="Method"
  {
    "jsonrpc": "2.0",
    "method": "call",
    "params": {
      "service": "common",
      "method": "login", 
      "args": [
        "db",
        "email",
        "password"
      ]
    }
  }
```

### Request

Login to the *`db`* database using the *`email`* login and *`password`* password.

``` json title="Request body"
{
  "jsonrpc": "2.0",
  "method": "call",
  "params": {
    "service": "common",
    "method": "login", 
    "args": [
      "prod",
      "email@example.com",
      "super_secret_password"
    ]
  }
}
```

### Response

!!! note

    The field *`result`* value contains the UID of the login email used as a parameter.

    This integer can then be used inside requests made to an instance.

``` json title="Response body"
{
  "id": null,
  "jsonrpc": "2.0",
  "result": 1
}
```

[^1]:
    Starting from Odoo v.14.0, API keys can be used instead of the user password. As a common security practice, API keys should be used instead of passwords when available.
[^2]:
    See [^1]
