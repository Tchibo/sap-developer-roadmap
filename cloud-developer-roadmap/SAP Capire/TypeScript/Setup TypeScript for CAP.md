---
tags:
  - typescript
  - intermediate
links:
  - "[[TypeScript]]"
source:
aliases:
---
To enhance type safety in your implemented business logic, it is recommended to use [[TypeScript]]. With the use of [[cds-models]], entities, views, and types defined in your database and service layers are automatically generated. These can then be referenced directly in your business logic, ensuring consistency and reducing runtime errors.

> [!todo] Outline the impact of using TypeScript on the project's build and deploy phase
> Evenn though Capire documentation is linked I would suggest to include your condensed insight into the impact of TypeScript on the build and deployment process of the app. As far as I understand it TypeScript is a development-support feature to catch type errors early on, at runtime though the plain JavaScript sources are executed?

Comprehensive documentation is linked below, offering detailed instructions and guidance on how to integrate [[TypeScript]] into your project.

**Summary**  
Utilizing [[TypeScript]] in [[SAP Capire]] projects ensures greater type safety and consistency by allowing direct access to generated entities and types from the data model. [[SAP Capire]] offers thorough documentation to support this integration.

**Sources**
- [SAP Capire - Using TypeScript](https://cap.cloud.sap/docs/node.js/typescript#using-typescript)