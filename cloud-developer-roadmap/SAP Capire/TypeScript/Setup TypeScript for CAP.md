---
tags:
  - typescript
  - intermediate
links:
  - "[[TypeScript]]"
source:
aliases:
---
To enhance type safety in your implemented business logic, it is recommended to use [[TypeScript]]. When using [[CDS Models]], entities, views, and types defined in your database and service layers are automatically generated. These can then be referenced directly in your business logic, ensuring consistency and reducing runtime errors.

TypeScript primarily serves as a development-time tool, catching type errors early. During the build phase, TypeScript code is transpiled into plain [[JavaScript]], which is executed at runtime. This means that while TypeScript improves developer productivity and code safety, the deployed application runs standard [[JavaScript]], so there is no additional runtime overhead. In terms of deployment, the build process must include the TypeScript compilation step, but otherwise the generated artifacts (services and modules) follow the same [[Domain Modelling|CAP]] deployment flow.

Comprehensive documentation is available to guide integration of [[TypeScript]] into your [[SAP Capire]] project, including setup, type generation, and recommended best practices.

**Sources**
- [SAP Capire - Using TypeScript](https://cap.cloud.sap/docs/node.js/typescript#using-typescript)