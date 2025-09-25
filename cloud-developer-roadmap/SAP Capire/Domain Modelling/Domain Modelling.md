---
tags:
  - cap-cds
  - cds
  - cdl
  - basic
links:
  - "[[SAP Capire|SAP Capire]]"
  - "[[Service Definition]]"
source: https://cap.cloud.sap/docs/
aliases:
  - CAP
  - cap
  - capire
  - Domain Model
---
Domain modeling in the [[SAP Capire|CAP]] Framework involves creating a conceptual data model that represents business objects, their [[relationships]], and rules within your [[application domain]]. In [[SAP Capire|CAP]], this is typically implemented using [[CAP CDS|CDS]], which provides a declarative language to define [[Domain Entites|entities]], [[Association|associations]], and services.

The [[SAP Capire|CAP]] domain model is usually organized into separate files, such as `schema.cds` for persistent data definitions and `service.cds` for the service layer exposing the model. During deployment, `schema.cds` is materialized into database tables, while `service.cds` becomes views or service endpoints, such as [[OData]] or [[REST API]]s, rendering the model for application consumption. This separation ensures that the domain model serves as a single source of truth, abstracting technical details of data storage while allowing the service layer to adapt to different consumer needs.

An important extension of the domain model in [[SAP Capire|CAP]] is Draft Handling, which allows users to work on data in an intermediate state before finalizing changes. By using the `@odata.draft.enabled` annotation on entities, [[SAP Capire|CAP]] automatically generates the required entities, including shadow draft tables and lifecycle actions such as `EDIT`, `ACTIVATE`, and `CANCEL`. Drafts are managed through [[OData v4]], maintaining separate draft and active versions of entities. Key benefits include optimistic locking to prevent conflicting edits, automatic draft cleanup, and the ability to add custom validations.

By combining a structured domain model with draft capabilities, [[SAP Capire|CAP]] ensures consistency, simplifies transactional workflows, and accelerates the evolution of business applications. Developers can focus on domain logic, while [[SAP Capire|CAP]] handles schema generation, service exposure, and draft lifecycle management automatically.

**Sources**
- [SAP Capire - CDL](https://cap.cloud.sap/docs/cds/cdl)
- [SAP Capire - Domain Modelling](https://cap.cloud.sap/docs/guides/domain-modeling)
- [SAP Capire - Performance Modeling](https://help.sap.com/docs/btp/sap-business-technology-platform/application-router?locale=en-US)
- [SAP Capire - Draft Support](https://cap.cloud.sap/docs/advanced/fiori#draft-support)
- [SAP Capire - Lean Draft](https://cap.cloud.sap/docs/node.js/fiori#lean-draft)