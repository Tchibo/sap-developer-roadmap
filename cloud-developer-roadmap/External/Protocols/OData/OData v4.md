---
tags:
  - odata
  - protocols
link: "[[OData]]"
---
OData V4 is a [[REST]]-based protocol that lets you access and manipulate data through simple URLs. Each segment of the URL defines what you want to read or change. For example:

```
/Books(1)?$select=title,author&$expand=publisher&$filter=year gt 2015&$top=10&$skip=20
```

Here `/Books(1)` addresses a single book by its key. The query `$select=title,author` restricts the attributes to be retrieved. With `$expand=publisher` the related publisher entity is included. `$filter=year gt 2015` narrows down the results. `$top=10` and `$skip=20` control paging. The HTTP verb defines the action: `GET` reads, `POST` creates, `PATCH` updates, and `DELETE` removes.