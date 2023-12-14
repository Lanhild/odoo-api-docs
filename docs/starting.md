# Story

The reason why this documentation exists is because Odoo doesn't provide any official specification or information for their HTTP API itself.

## Context and Usage

First and foremost, it is important to know that this API only has a single endpoint and only the request payload changes. Thus why, this documentation couldn't be conveniently made into an OpenAPI spec.

All interactions made with the API are `POST` requests and most of them must pass the authentication.

## Use Cases

The following are potential use cases of the API that could apply to the common user:

- Software applications where using code libraries isn't possible
- SaaS applications such as [n8n and it's Odoo node](https://github.com/n8n-io/n8n/tree/master/packages/nodes-base/nodes/Odoo)
- Common testing or data filtering

### Resources

Useful links I came across while writing this documentation:

- [n8n's Odoo node - Specifies some of the syntax to be used for requests](https://github.com/n8n-io/n8n/tree/master/packages/nodes-base/nodes/Odoo)
- [Odoo - *Web Services*](https://www.odoo.com/documentation/16.0/developer/howtos/web_services.html?highlight=jsonrpc#json-rpc-library)
- [Odoo - *External API*](https://www.odoo.com/documentation/16.0/developer/reference/external_api.html)
- [OdooRPC's documentation *Python module documentation*](https://pythonhosted.org/OdooRPC)
- [openobject-server 7.0 - *Source Code*](http://bazaar.launchpad.net/~openerp/openobject-server/7.0/view/head:/openerp/osv/orm.py#L2325)
