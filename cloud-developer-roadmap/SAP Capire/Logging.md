---
tags:
  - logging
  - basic
links:
source:
aliases:
---
Logging in [[SAP Capire]] plays a fundamental role in monitoring and diagnosing the behavior of services within cloud-native applications. By default, the framework offers structured and consistent logging. Developers can extend this by implementing [[Custom Logger|custom logging]] logic within their services. This can be useful for capturing domain-specific events, enhancing observability, or tracking key business processes.

Applications developed with [[SAP Capire]] can be deployed to environments that support [[SAP Application Logging]] and [[SAP Cloud Logging]], which provides contextual log messages. These options make it possible to trace issues more effectively and ensure operational transparency in both development and production scenarios.


**Sources**
- [SAP Capire - `cds.log()`](https://cap.cloud.sap/docs/node.js/cds-log#minimalistic-logging-facade)