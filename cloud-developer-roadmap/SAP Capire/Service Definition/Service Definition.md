---
tags:
  - basic
links:
  - "[[SAP Capire|SAP Capire]]"
  - "[[Domain Modelling]]"
source:
aliases:
---
The Service Layer in the [[SAP Capire|CAP]] Framework defines the API contracts for accessing your application's functionality and exposes the [[domain model]] through standardized interfaces, ensuring consistent access patterns while maintaining a separation of concerns between the core data model and external consumers.

In [[SAP Capire|CAP]], services are declared using [[CAP CDS|CDS]] service definitions, which specify the entities to expose and the allowed operations. The Service Layer acts as a controlled gateway between clients and the application's core business logic, enforcing consistency, validation, and access rules.

Service [[Views & Projections]] are defined in the `service.cds` file. When deployed to a database such as [[PostgreSQL on SAP BTP]] or [[SAP HANA Cloud]], these projections are materialized as actual database artifacts. They are no longer purely virtual but become database views or other deployable objects, allowing clients to interact with them like standard tables while maintaining selection, aggregation, or transformation logic. [[SAP Capire|CAP]] automatically maps operations on these projections back to the underlying domain entities, ensuring that data modifications are persisted correctly and access controls are applied.

By materializing projections as database artifacts, [[SAP Capire|CAP]] ensures efficient, consistent access to data while preserving a clear separation between the domain model and service interfaces.

**Sources**
- [SAP Capire - Providing Services](https://cap.cloud.sap/docs/guides/providing-services#providing-services)