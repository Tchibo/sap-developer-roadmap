---
tags:
  - cap-cds
  - cds
  - cdl
  - basic
links:
source:
aliases:
---
Entity exposure in [[SAP Capire]] refers to the process of making data models (entities) accessible through a service, so they can be consumed via [[API]]s such as [[OData]]. There are two main approaches:
- **Implicit exposure**
  All entities defined within a service are made available by default, without further specification.
- **Explicit exposure**
  Only those entities that are explicitly listed or projected in the service definition are made accessible.
This mechanism allows developers to control precisely which parts of the data model are accessible to external consumers.

**Summary**  
Entity exposure in [[SAP Capire]] determines which data models are made available through a service either automatically (implicit) or by explicit selection (explicit) enabling controlled access for external consumers.

**Sources**
- [SAP Capire - Events to Auto-Exposed Entites](https://cap.cloud.sap/docs/guides/security/authorization#events-and-auto-expose)