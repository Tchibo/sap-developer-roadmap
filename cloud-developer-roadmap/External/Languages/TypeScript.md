---
tags:
  - language
  - external
  - intermediate
links:
  - "[[Node.js]]"
source:
aliases:
  - TS
  - ts
---
TypeScript brings clear benefits when developing with the [[SAP Capire]]. Unlike plain [[JavaScript]], it introduces [[static typing]] which helps catch errors early and provides stronger contracts between services, entities and [[API]]s defined in [[CDS Models|CDS models]]. With generated type definitions from [[CDS]], developers can work with auto-completion, type hints and compile-time validation of queries. This ensures that the data model defined in [[CDS]] remains consistent throughout the application and reduces the risk of runtime issues.

In larger teams, TypeScript also improves collaboration as explicit types act as living documentation. Code becomes easier to read and maintain, which simplifies onboarding and supports long-term stability of [[SAP Capire|CAP]] projects. While TypeScript adds a compilation step, [[SAP Capire|CAP]] provides dedicated tooling and definitions that integrate smoothly into the workflow. Developers do not need to be TypeScript experts to benefit from these features, as even basic use of types and interfaces significantly enhances reliability.

For prototypes or small applications [[JavaScript]] may be sufficient, but for scalable and enterprise-grade solutions TypeScript is the recommended option to strengthen the link between [[CDS Models|CDS models]] and application logic.

**Sources**
- [SAP Capire - Using TypeScript](https://cap.cloud.sap/docs/node.js/typescript#using-typescript)
- [Roadmap.sh - TypeScript](https://roadmap.sh/typescript)