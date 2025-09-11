---
tags:
  - logging
  - rework
  - custom-handler
  - advanced
links:
source:
aliases:
---

> [!toDo] Reference to SAP Cloud Logging Service as logging destination
> Do mention the fact that destination for transporting logs at Tchibo is the SAP Cloud Logging Service. Just to make sure that no one chooses an ABAP backend to create an Application Log or builds a custom CAP logging persistence.

The [[SAP Capire]] framework enables developers to implement custom logging solutions tailored to their specific requirements. Out of the box, the framework provides support for the popular [winston](https://www.npmjs.com/package/winston) logging library, allowing for flexible and extensible logging configurations.

**Sources**
- [SAP Capire - cds.log](https://cap.cloud.sap/docs/node.js/cds-log#minimalistic-logging-facade)
- [SAP Capire - Custom Logging](https://cap.cloud.sap/docs/node.js/cds-log#custom-loggers)