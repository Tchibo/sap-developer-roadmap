---
tags:
  - sap-capire
  - basic
links:
  - "[[SAP Capire|SAP Capire]]"
source:
aliases:
---
**What is [[SAP Capire]]?**
The [[SAP Capire|SAP Cloud Application Programming Model]] is a framework for building cloud-native applications. It provides tools and a domain-driven approach to simplify development, supporting both **[[Node.js]]** and **[[Java]]**. Key features include Core Data Services ([[CDS]]) for modeling, seamless integration with [[SAP HANA]] and [[SAP Fiori]], and a declarative style that separates concerns.

**What characterizes the [[SAP Capire]] Framework?**
The framework is centered around a domain-driven, declarative development style. It uses a layered architecture with a clear separation between data, service, and UI layers. [[CDS]] is used for data modeling, and services are automatically exposed as [[OData]] or [[REST API]]s. This approach allows developers to focus on business logic rather than technical details.

**Interfaces with SAP RAP**
[[SAP Capire]] and [[RAP]] share similar architectural patterns, though they use different technologies ([[Node.js]]/[[Java]] vs. [[ABAP]]). Both use [[CDS]] for data modeling and integrate with [[Fiori Elements]] for the UI.

> [!todo] Similarities with RAP are not the reason
> CAP came about first and RAP adopted its ideas in a slightly more elaborate / prescriptive way. So the similarity with RAP is consequential, not causal.

**Summary**
The **SAP [[SAP Capire|Cloud Application Programming Model]]** offers a structured approach for developing cloud-native applications. Its focus on declarative modeling and automatic service exposure allows developers to concentrate on the business domain. The similarities with [[SAP RAP]] make it a strong foundation for modern SAP development on the [[SAP BTP]].

**Sources**
- [SAP Capire - Documentation](https://cap.cloud.sap/docs/)
- [SAP Help Portal – SAP BTP](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b)
- [GitHub – SAP-samples/cloud-cap-samples](https://github.com/SAP-samples/cloud-cap-samples)
- [GitHub - Fiori Elements Sample](https://github.com/SAP-samples/fiori-elements-feature-showcase?tab=readme-ov-file#selection-variant)