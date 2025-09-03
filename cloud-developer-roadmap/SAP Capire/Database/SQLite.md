---
tags:
  - database
links:
  - "[[Databases]]"
source:
aliases:
  - sqlite
---
The [[SAP Capire]] framework allows the use of **SQLite** as a database, commonly in the context of **local development and testing**. SQLite runs without the need for an external database server and can be used either in persistent or in-memory mode.

> [!WARNING]
> SAP **does not intend** SQLite to be used in production environments. Its should be  limited to development and testing scenarios.

Database configuration is handled using the `cds.requires`-section in the `package.json`. This makes it possible to define different database backends depending on the runtime environment:
```json
{

  "cds": {
    "requires": {
      "db": {
        "[production]": {
          "kind": "postgres",
          "dialect": "postgres"
        },
        "[development]": {
          "kind": "sqlite"
        }
      }
    }
  }
}
```
In this setup, the application connects to SQLite in the development environment and uses [[PostgreSQL on SAP BTP]] in production. This allows [[SAP Capire|Capire]] projects to run locally without requiring external database infrastructure.

**Sources**
- [SAP Capire - SQLite](https://cap.cloud.sap/docs/guides/databases-sqlite)