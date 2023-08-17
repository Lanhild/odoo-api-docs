# Welcome

This is an **unofficial** documentation of Odoo's JSON-RPC API.

You can use this documentation as a reference point for any operation you wish to perform using the API of an Odoo instance.

## Index

1. [Getting started - *Make sure to read this section before starting*](./common/common-parameters-in-a-request.md)
2. [Login to a given database](./authentication/how-to-login-to-a-given-database.md)
3. [CRUD operations](./crud/perform-crud-operations.md)

## Important notice

First and foremost, it is important to know that this API has only one path and only the request payload changes[^1].

Thus why this documentation was not made in an OpenAPI specification.

## More documentation pages, why?

Using the HTTP `/jsonrpc` API on a daily basis, I could no longer bear with the frustration that Odoo didn't provide any information or specification for the web API of their own software.

That's when I decided to write this documentation myself.

You can help me improve the API documentation whether it's by making changes to the definition itself or by submitting suggestions.

## Use cases of the API

The following are use cases I personally have, but that can apply to a broader population of users:

- Software applications where using code libraries isn't possible
- SaaS applications such as [n8n and it's Odoo node](https://github.com/n8n-io/n8n/tree/master/packages/nodes-base/nodes/Odoo)

### Resources

Useful links I came across while writing this documentation:

- [n8n's Odoo node - Specifies some of the syntax to be used for requests](https://github.com/n8n-io/n8n/tree/master/packages/nodes-base/nodes/Odoo)
- [Odoo - *Web Services*](https://www.odoo.com/documentation/16.0/developer/howtos/web_services.html?highlight=jsonrpc#json-rpc-library)
- [Odoo - *External API*](https://www.odoo.com/documentation/16.0/developer/reference/external_api.html)

[//]: # "Footnotes"

[^1]: ./common/common-parameters-in-a-request.md#notice
