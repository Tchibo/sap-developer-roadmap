---
tags:
  - service
  - business-logic
  - java
links:
  - "[[SAP Capire|SAP Capire]]"
  - "[[Choose a backend]]"
  - "[[Java]]"
  - "[[Spring Boot]]"
source:
aliases:
---
The [[SAP Capire]] Framework offers both [[Node.js]] and [[Java]] as supported runtimes. While [[Java]] runs on [[Spring Boot]] and provides an enterprise-ready environment with strong typing and tooling, it is not the preferred option in many project settings. Since [[SAPUI5]] already requires developers to work with [[JavaScript]] or [[TypeScipt]] for [[SAP Fiori extensions]], adding [[Java]] as a third language can increase complexity without significant benefit. For this reason, most [[SAP Capire|CAP]] projects focus on [[Node.js]], which integrates seamlessly with [[CDS Models|CDS models]], provides first-class [[TypeScipt]] support, and aligns closely with the broader [[SAP]] ecosystem. Concentrating on [[Node.js]] allows development teams to avoid language fragmentation and build both frontend and backend capabilities with [[JavaScript]] and [[TypeScript]].

**Sources**
- [CAP Java – Getting Started](https://cap.cloud.sap/docs/java/getting-started)