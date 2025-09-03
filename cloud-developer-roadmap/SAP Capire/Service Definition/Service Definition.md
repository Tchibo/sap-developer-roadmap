---
tags:
  - basic
links:
  - "[[SAP Capire|SAP Capire]]"
  - "[[Domain Modelling]]"
source:
aliases:
---
The Service Layer in the [[SAP Capire]] Framework defines the API contracts for accessing your application's functionality and exposes the [[domain model]] through standardized interfaces.

In [[SAP Capire]], services are declared using [[CDS]] service definitions, which specify which entities are exposed and what operations are allowed. The Service Layer acts as a controlled gateway between clients and your application's core business logic.

Service [[Views & Projections]] in the Service Layer are not persisted as separate database objects. Instead, they provide virtual views of the underlying [[domain entities]], which are mapped to persistent tables. When clients interact with these projections, [[SAP Capire]] translates the operations to the corresponding domain entities, ensuring data modifications are properly stored while maintaining the projection's view semantics and access controls.

The Service Layer ensures consistent access patterns while maintaining a separation of concerns between your domain model and external interfaces.

**Sources**
- [SAP Capire - Providing Services](https://cap.cloud.sap/docs/guides/providing-services#providing-services)