---
tags:
  - frontend
  - basic
links:
source:
aliases:
---
The [[SAP Capire]] Framework supports serving user interfaces in addition to exposing APIs. This allows for building frontend applications that interact directly with the backend services of a [[SAP Capire]] project. While any frontend technology can be used, the recommended approach is to build UIs with [[SAP Fiori Elements]], which is natively supported and integrates seamlessly with [[SAP Capire]]'s metadata-driven architecture.

[[Fiori Elements]] uses [[CDS annotations]] from the [[SAP Capire]] backend to automatically generate consistent UIs. These annotations provide the metadata needed to render components like tables and forms without manual coding, reducing development time and keeping the UI aligned with the backend.

In special cases, alternatives like the [[Flexible Programming Model]] or [[freestyle SAPUI5]] applications can be used, but these are typically for scenarios requiring more flexibility. Whenever possible, [[Fiori Elements]] is preferred due to its tight integration with [[SAP Capire]].

**Summary**  
The [[SAP Capire]] Framework supports building UIs on top of backend services. [[Fiori Elements]] is the recommended approach due to its native support and use of [[CDS]] annotations for efficient UI generation. Alternatives like [[Flexible Programming Model]] or [[freestyle UI5]] should only be used in exceptional cases.

**Sources**
- [SAP Capire - Serving Fiori UIs](https://cap.cloud.sap/docs/advanced/fiori)
- [SAP Capire - Serving UIs](https://cap.cloud.sap/docs/get-started/in-a-nutshell#fiori)