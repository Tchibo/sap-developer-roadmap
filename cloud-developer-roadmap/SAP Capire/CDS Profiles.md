---
tags:
  - basic
links:
  - "[[SAP Capire|SAP Capire]]"
source:
aliases:
---
CDS Profiles in the [[SAP Capire]] framework allow you to manage different configuration environments for an application. A profile bundles a set of configuration settings that can be activated to switch between variants for development, testing, and production.

With [[CDS]] profiles, you can specify which database, authentication, or external services to use in a given environment. For example:
- A **development profile** might use a local [[SQLite]] database and mock authentication for fast local testing.
- A **production profile** would connect to a productive [[SAP HANA Cloud]] database and use the [[XSUAA]] service for authentication.
Profiles are typically defined in a configuration (`package.json` or `.cdsrc.json`) file and activated at runtime using environment variables or [[CLI]] arguments, allowing you to switch configurations without changing the application code.
da
**Sources**
- [SAP Capire - Configuration Profiles](https://cap.cloud.sap/docs/node.js/cds-env#profiles)