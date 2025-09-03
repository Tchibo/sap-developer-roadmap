---
tags:
  - basic
links:
source:
aliases:
---
One of the key features of the [[SAP Capire]] Framework is the ability to define and implement custom logic through event handlers in [[Node.js]]. Event handlers allow developers to react to specific events, such as CRUD operations on entities, and to extend or customize the behavior of their applications.

In a typical [[SAP Capire|CAP]]  [[Node.js]] service, event handlers are implemented by listening to events such as `READ`, `CREATE`, `UPDATE`, or `DELETE` on entities defined in the data-model. The event handlers can be used for tasks like data validation, enriching responses, or integrating with external systems.

**Example: Implementing a Node.js Event Handler in CAP** 
Suppose we have an entity `Books` and we want to add custom logic every time a new book is created, e.g., automatically setting the `createdAt` timestamp. The following code shows how to implement this in a [[SAP Capire|CAP]] [[Node.js]] service:

> [!note]
> This example is intended only to demonstrate how such a handler could be implemented. The possibilities for implementing logic are not limited to simply setting default values.

```js
// srv/cat-service.js
const cds = require('@sap/cds');

module.exports = cds.service.impl(async function() {
  this.after('CREATE', 'Books', (req) => {
    // Automatically set createdAt timestamp
    req.forEach(book => {
      book.createdAt = new Date().toISOString();
    });
  });
});
```

In this example, the event handler is registered using the `after` hook for the `CREATE` event on the `Books` entity. For every book created, it sets the `createdAt` property to the current timestamp.

**Summary**  
[[Node.js]] event handlers in the [[SAP Capire]] Framework enable developers to react to data events, customize business logic, and extend standard operations in a flexible way. This approach helps ensure clean separation of concerns and maintainable code in SAP cloud applications.

**Sources**
- [SAP Capire - Best Pratices: Events](https://cap.cloud.sap/docs/about/best-practices#events)
- [SAP Capire - Application Services](https://cap.cloud.sap/docs/node.js/app-services#application-services)