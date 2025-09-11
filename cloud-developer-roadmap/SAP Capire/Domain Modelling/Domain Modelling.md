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
> [!toDo] Reference to how the domain model is materializing in CAP
> It helped me a lot at the time when I understood at the time that schema.cds contained the domain model (becoming database tables at time of deployment to be database) and service.cds contained the service definition for rendering of the model (becoming views at time of deployment to the database). I would mention some of that here.

Domain Modelling in the SAP [[SAP Capire|Cloud Application Programming]] Framework refers to the creation of a conceptual data model that represents the business objects, their [[relationships]], and rules in your [[application domain]] and is responsible for the definition of [[persistent tables]].

In the [[SAP Capire|CAP]] context, this is typically implemented through [[Core Data Services]], which provides a declarative language for defining [[Domain Entites|entities]], [[Association|associations]], and services. The [[Domain Modelling|Domain Model]] forms the foundation of your application and abstracts the technical details of data storage.

The [[Domain Modelling|Domain Model]] serves as the single source of truth for your [[application logic]] and simplifies the maintenance and evolution of your systems.

**Sources**
- [SAP Capire - CDL](https://cap.cloud.sap/docs/cds/cdl)
- [SAP Capire - Domain Modelling](https://cap.cloud.sap/docs/guides/domain-modeling)
- [SAP Capire - Performance Modeling](https://help.sap.com/docs/btp/sap-business-technology-platform/application-router?locale=en-US)