---
tags:
  - database
  - basic
links: []
source: https://cap.cloud.sap/docs/guides/databases
---
The [[SAP Capire]] Framework offers the possibility to use different databases or to deploy the project with different databases without having to make major changes to the implemented business logic or changes to the data schema. This is made possible by the fact that [[data modelling]] is not done in a database-specific "language", but with [[CAP CDS]]. The tables, views... are converted into a [[CSN]] target schema using the [[cds-dbs]] plugin, on the basis of which the database schema with relations etc. is built for the configured target database.

**Sources**
- ==[DB - Decision TCH](https://wiki.tchibo-intranet.de/x/VoJtNw)==
- [[PostgreSQL on SAP BTP]]
- [[SAP HANA Cloud]]
- [[SAP HANA Native]]