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
Using the [[cds CLI]], you can deploy your database schema along with project-local data stored in CSV files. These CSV files are often used for configuration, enumerations, or other reference data that needs to be available in the connected database (e.g. using value-helps with static data). Deployment can target a local [[SQLite]] database or an external database such as the [[PostgreSQL]] database used in [[SAP Capire]] projects.

When the database is started repeatedly, the CSV data is redeployed each time. This ensures that any required reference data is consistently available, but it also means that existing data may be overwritten depending on the deployment strategy.

**Sources**
- [SAP Capire](https://cap.cloud.sap/)
- [SAP Capire - Databases](https://cap.cloud.sap/docs/guides/databases)