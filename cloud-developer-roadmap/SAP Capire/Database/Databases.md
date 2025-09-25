---
tags:
  - database
  - basic
links: []
source: https://cap.cloud.sap/docs/guides/databases
---
The [[SAP Capire]] Framework allows projects to be developed independently of the underlying database. This flexibility is achieved because data modelling is performed in [[CAP CDS]] rather than a database-specific language. The CDS definitions for tables, views, and relationships are converted into a [[CSN]] target schema using the [[cds-dbs]] plugin, which is then used to generate the database schema for the configured target database.

At Tchibo, we currently use [[PostgreSQL]] on SAP BTP, Hyperscaler Edition, as the standard database for [[SAP Capire]] projects. This provides a reliable and scalable foundation while maintaining the flexibility to adapt to other databases in the future if needed.

**Sources**
- ==[DB - Decision TCH](https://wiki.tchibo-intranet.de/x/VoJtNw)==
- [[PostgreSQL on SAP BTP]]
- [[SAP HANA Cloud]]