---
tags:
  - test
  - integration-test
  - intermediate
links:
  - "[[Testing]]"
  - "[[SAP Business Application Studio]]"
source:
aliases:
---
Hybrid testing in [[SAP Capire]] projects involves testing your application in a local development environment while integrating with externally deployed services, such as a database or an [[OData]] service from another SAP system. The goal is to validate that your application behaves correctly when interacting with services that resemble the target deployment environment.

[[SAP Capire]] and [[SAP BTP]] enable this form of testing. Developers can run their [[SAP Capire]] project locally and bind it to external services using `cds bind` or `cf bind-local`, which allows local access to remote service data.

> [!TIP] Tip
> When testing with on-premise systems, it is recommended to use the [[SAP Business Application Studio]]. It includes an [HTTP proxy](https://sap.github.io/cloud-sdk/docs/js/guides/bas) that resolves destinations using the [[SAP Cloud Connector]], simplifying the setup for external services.

A step-by-step guide for hybrid testing can be found in the [official CAP documentation](https://cap.cloud.sap/docs/advanced/hybrid-testing#hybrid-testing).

**Summary**
Hybrid testing allows [[SAP Capire]] developers to run their application locally while connecting to external services, ensuring compatibility with production-like environments. Tools like [[SAP Business Application Studio]] simplify this process, especially for on-premise systems.

**Sources**
- [SAP Capire - Hybrid Testing](https://cap.cloud.sap/docs/advanced/hybrid-testing#hybrid-testing)
- [SAP Cloud SDK - Connecting to external systems](https://sap.github.io/cloud-sdk/docs/js/guides/bas)