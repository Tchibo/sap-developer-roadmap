---
tags:
  - cap-cds
  - basic
links:
  - "[[SAP CDS]]"
---
Core Data Services ([[CDS]]) are a central element of the [[SAP Capire|CAP]] framework, providing a standardized way to define and manage the data model for cloud-native applications. With CDS, developers can describe entities, their attributes, types, and relationships in a concise, declarative language, independent of the underlying database technology. This allows CAP to automatically generate database schemas and service definitions based on the model, ensuring consistency between the data layer and the application logic.

In CAP, CDS serves a dual purpose. First, it defines the persistent data model for the application, which the framework translates into database tables, views, and relationships when deploying to a target database such as [[SAP HANA]] or [[PostgreSQL on SAP BTP]]. Any changes in the CDS model are reflected in the database schema during deployment, which simplifies schema evolution and reduces manual database management.

Second, CDS defines service models that expose entities to consumers, for example via [[OData]] or [[REST API]] endpoints. Projections of entities can be created to tailor the data structure for specific use cases, such as different views for read or write operations. This integration allows CAP to automatically handle the service layer, mapping requests to the underlying database and applying business logic defined in custom event handlers or TypeScript/Java code.

Within the [[SAP Capire]] framework, CDS is the backbone for both data persistence and service definition. It enables a declarative, model-driven development approach where changes in the data model are seamlessly propagated to services and the database. This ensures consistency, reduces boilerplate code, and accelerates the development of enterprise-ready cloud applications.

**Sources**
- [SAP Capire - Core Data Services (CDS)](https://cap.cloud.sap/docs/cds/)