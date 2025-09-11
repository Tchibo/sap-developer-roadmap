---
tags:
  - custom-handler
  - business-logic
  - basic
links:
  - "[[Add Business Logic]]"
source:
aliases:
---
The [[SAP Capire]] framework provides developers with the flexibility to extend standard service behavior by implementing custom business logic. This is achieved through **custom handlers**, which allow you to intercept and enhance the lifecycle of your services, such as reading, creating, updating, or deleting data.

> [!toDo] There is a system to how extensions can be registered
> It helped me at the time to understand that registration of handlers can be 'Before', 'On' or 'After' the HTTP verb action beeing performed, detailed by entity. That applies to all verbs in HTTP CRUD. It also needs to sink in that if I e.g. want to amend the result of a managed GET request I can register an 'After' handler to amend the response to the GET request. Likewise it is good to know that when you register an 'On' Handler then the managed handler is replaced. You've got most of this in the subtopic 'Node.js Custom Handler' document.

Custom handlers are typically used to:
- **Override default service behavior**
  For example, to change how data is processed during certain events.
- **Add business validations**
  Ensure data integrity and enforce business rules before data is persisted.
- **Implement custom calculations or enrich responses** 
  For example, adding calculated fields or enriching the response with additional data.

In [[SAP Capire]], you can "mount" (register) these handlers on specific lifecycle events (such as `before CREATE`, `after UPDATE`, or `on DELETE`) for your entities or services. This event-driven approach provides precise control over when your logic is executed.

A simple example of a custom handler in [[SAP Capire]] using [[Node.js]]:
```js
module.exports = (srv) => {
  srv.before('CREATE', 'Books', (req) => {
    // Example: Validate or modify data before creating a Book
    if (!req.data.title) {
      req.reject(400, 'Title is required');
    }
  });

  srv.after('READ', 'Books', (each) => {
    // Example: Add a calculated field after reading Books
    each.isExpensive = each.price > 100;
  });
};
```

This modular, event-driven model makes it easy to implement robust, reusable business logic in [[SAP Capire]] projects.


> [!toDo] This document is a bit long, drop the following paragraph to shorten
> The most important message has been provided at this point in time. The next paragraph is adding detail that blurs the picture in my opinion and exceeds the length that's meaningful in roadmap.sh. 

Beyond business logic, [[SAP Capire|CAP]] also allows for further extensibility:

- **Custom Authentication Handlers**
  You can implement your own authentication and authorization logic using custom handlers or by registering middleware. This makes it possible to integrate with custom identity providers or enforce specialized access control rules beyond [[SAP Capire|CAP]]’s built-in authentication.
- **Custom `server.js`:** 
  By providing your own `server.js` file, you gain full control over the [[SAP Capire|Capire]] application startup process. This lets you mount custom [[Express.js]] middleware, add additional routes, or configure the underlying [[HTTP]] server as needed for your application scenario.

**Summary**  
Custom [[Node.js]] handlers in [[SAP Capire]] allow developers to extend and customize service behavior by hooking into specific lifecycle events. They enable validation, enrichment, and business logic implementation directly in the service layer, providing full control over how data is processed and handled in your [[SAP Capire]] applications.

**Sources**
- [SAP Capire - Providing Services (Custom Logic)](https://cap.cloud.sap/docs/guides/providing-services#custom-logic)