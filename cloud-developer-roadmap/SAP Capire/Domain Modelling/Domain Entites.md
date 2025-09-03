---
tags:
  - cds
  - data-modelling
  - cap-cds
  - cdl
  - basic
links:
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/guides/domain-modeling#domain-entities
aliases:
  - entity
  - table
  - entities
---
Domain entities define the core business objects of a domain and represent key concepts such as products, customers, or orders. In the[[SAP Capire]] Framework, entities are modeled using [[CDS|Core Data Services]] and serve as the primary building blocks for [[Domain Modelling|domain modelling]]. Each entity consists of fields that describe its attributes and relationships to other entities. When persisted, entities typically map to tables in a relational database, with each entity instance becoming a row. Entities are named according to namespaces, which help avoid naming conflicts and organize models into logical domains. It is recommended to use meaningful and concise names that reflect the business semantics of the domain.

Entities can also reference type definitions to reuse commonly used data types and structures, promoting consistency and maintainability across the model.

**Summary**  
Domain entities are the main business objects modeled with [[CDS]] in the [[SAP Capire]] Framework. They define the structure, attributes, and relationships of data relevant to a domain. In persistence, entities usually correspond to database tables. Namespaces and type definitions support clear organization and reusability in domain modeling.

**Sources**
- [SAP Capire - Namespaces](https://cap.cloud.sap/docs/guides/domain-modeling#namespaces)
- [SAP Capire - Domain Entities](https://cap.cloud.sap/docs/guides/domain-modeling#domain-entities)
- [SAP Capire - Entites & Type Definitions](https://cap.cloud.sap/docs/cds/csn#type-definitions)