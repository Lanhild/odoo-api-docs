# Search Operators

The `search_read` method supports filters formatted as tuples of three elements: a *`field`*, an *`operator`*, and a *`value`*.

``` json title="Syntax"
[
    [
        "field",
        "operator",
        "value"
    ]
]
```

- *`field`* is a string containing the name of the field of the object model to search for.
- *`operator`* is a string containing the operator from the list: ``=, !=, >, >=, <, <=, like, ilike, in, not in, child_of``.
- *`value`* is the value to which the field is compared, following the type of its operator.
