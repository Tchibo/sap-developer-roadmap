---
tags:
  - database
  - basic
links: []
source: https://cap.cloud.sap/docs/guides/databases
---
The [[SAP Capire]] Framework allows projects to be developed independently of the underlying database. This flexibility is achieved because data modelling is performed in [[CAP CDS]] rather than a database-specific language. The CDS definitions for tables, views, and relationships are converted into a [[CSN]] target schema using the [[cds-dbs]] plugin, which is then used to generate the database schema for the configured target database.

**Sources**
- [[PostgreSQL on SAP BTP]]
- [[SAP HANA Cloud]]
