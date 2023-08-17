# Welcome

This is an **unofficial** documentation of Odoo's JSON-RPC API.

You can use this documentation as a reference point for any operation you wish to perform using the API of an Odoo instance.

## Navigation

In order to navigate through this documentation, the sidebar can be used as a reference point.

## Important notice

**First and foremost**, it is important to know that this API has only one path and only the request payload changes.

Thus why this documentation was not made in an OpenAPI specification.

## More documentation pages, why?

Since Odoo does not provide any information or specification for the web API of their own software, this documentation site has been put up.

Contributions are welcome whether it's by making changes to the definition itself or by [submitting suggestions](https://github.com/Lanhild/odoo-jsonrpc).

## Use cases of the API

This API acts like a REST API in the way that it can used for CRUD operations.

The following are potential use cases of the API that could apply to the common user:

- Software applications where using code libraries isn't possible
- SaaS applications such as [n8n and it's Odoo node](https://github.com/n8n-io/n8n/tree/master/packages/nodes-base/nodes/Odoo)

### Resources

Useful links I came across while writing this documentation:

- [n8n's Odoo node - Specifies some of the syntax to be used for requests](https://github.com/n8n-io/n8n/tree/master/packages/nodes-base/nodes/Odoo)
- [Odoo - *Web Services*](https://www.odoo.com/documentation/16.0/developer/howtos/web_services.html?highlight=jsonrpc#json-rpc-library)
- [Odoo - *External API*](https://www.odoo.com/documentation/16.0/developer/reference/external_api.html)
