---
tags:
  - protocols
  - api
  - service
  - odata
  - open-api
  - async-api
links:
  - "[[Service Definition]]"
source: https://cap.cloud.sap/docs/advanced/publishing-apis/
aliases:
---
The [[SAP Capire]] Framework provides developers with the flexibility to choose from a variety of adapters that determine how services are exposed and consumed. With these adapters, you can select one or more protocols for your services, ensuring they communicate in ways that best fit specific integration scenarios or client needs. Out of the box, [[SAP Capire]] supports adapters for [[OData v4]] (the default protocol), [[REST]], and [[GraphQL]], making it easy to connect [[SAP Capire|CAP]]-based services to diverse frontends, tools, and third-party systems.

In addition to these, [[SAP Capire]] also supports exposing services via the **WebSocket** protocol, using either the WebSocket standard or Socket.IO. This enables real-time, event-driven communication ideal for use cases like chat applications or live notifications. WebSocket support is available for Node.js-based [[SAP Capire|CAP]] projects, expanding the integration options for interactive applications.

**Summary**  
[[SAP Capire]] enables services to be exposed over multiple protocols including [[OData v4]], [[REST]], [[GraphQL]], and [[WebSocket]] using configurable adapters. This flexibility allows integration with a wide range of clients and systems, supporting both traditional and real-time communication scenarios.

**Sources**
- [SAP Capire - cds.serve: Protocols](https://cap.cloud.sap/docs/node.js/cds-serve#cds-protocols)
- [SAP Capire - Protocols/APIs](https://cap.cloud.sap/docs/advanced/publishing-apis/)
- [SAP Capire - WebSocket Protocol](https://cap.cloud.sap/docs/plugins/#websocket)
- [DJ Adams - OData and REST calls w/ CAP](https://qmacro.org/blog/posts/2024/07/24/automatic-validation-in-odata-and-rest-calls-with-cap/)