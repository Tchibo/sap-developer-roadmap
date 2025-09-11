---
tags:
  - deployment
  - database
  - basic
links:
  - "[[Databases]]"
  - "[[Add local data]]"
  - "[[Deployment]]"
  - "[[cds CLI]]"
source:
aliases:
---
> [!toDo] Purpose to deploy local data
> Do mention the purpose to use project-local .csv files whose content is deployed to the connected database, e.g. configuration, enumerations. Mention how deployment behaves in repeated database startup.

Using the [[cds CLI]], you can deploy your current database schema along with the corresponding local data files from CSV files. You can define the deployment target as either a local [[SQLite]] database or an external database, such as the [[PostgreSQL]] database used in [[SAP Capire]] projects.

For detailed information about limitations and additional relevant considerations, it is recommended to consult the respective database documentation in the official SAP Capire documentation.

**Sources**
- [SAP Capire](https://cap.cloud.sap)
- [SAP Capire - Databases](https://cap.cloud.sap/docs/guides/databases)