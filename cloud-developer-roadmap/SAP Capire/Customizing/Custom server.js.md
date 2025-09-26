---
tags:
  - custom-handler
  - advanced
links:
  - "[[Custom Logger]]"
source:
aliases:
---
The [[SAP Capire]] Framework allows developers to define a custom `server.js` (or `server.ts` for [[TypeScript]] projects) inside the `srv` directory. This capability enables you to centrally implement custom or advanced features such as:
- Custom or extended logging mechanisms
- Integration of custom [[middleware]]
- Handling logic based on server lifecycle events

By providing a custom server implementation, you gain full control over the server's behavior and can hook into various stages of the application's lifecycle. This makes it possible to adapt and extend the standard runtime to suit specific project requirements, such as implementing cross-cutting concerns, initializing resources, or reacting to events during startup and shutdown.

**Summary**  
A custom `server.js` in [[SAP Capire]] projects empowers developers to integrate logging, middleware, and lifecycle event handling in a centralized and flexible manner, extending the framework’s capabilities beyond the default behavior.

**Sources**
- [SAP Capire – Custom server.js](https://cap.cloud.sap/docs/node.js/cds-serve#custom-server-js
- [SAP Capire – Server Lifecycle Events](https://cap.cloud.sap/docs/node.js/cds-server#lifecycle-events)