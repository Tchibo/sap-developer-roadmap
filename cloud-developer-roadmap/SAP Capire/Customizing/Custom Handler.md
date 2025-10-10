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
The [[SAP Capire]] framework provides developers with the flexibility to extend standard service behavior by implementing custom business logic. This is achieved through custom handlers, which allow you to intercept and enhance the lifecycle of your services, such as reading, creating, updating, or deleting data. Handlers can be registered before, on, or after a specific HTTP verb action, and this applies to all CRUD operations.
- **Before handlers** run prior to the standard processing, ideal for validations or modifying input data.
- **On handlers** replace the managed behavior entirely, giving full control over the operation.    
- **After handlers** execute after the managed logic, useful for enriching responses or adding calculated fields, such as modifying the result of a GET request.

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

**Sources**
- [SAP Capire - Providing Services (Custom Logic)](https://cap.cloud.sap/docs/guides/providing-services#custom-logic)