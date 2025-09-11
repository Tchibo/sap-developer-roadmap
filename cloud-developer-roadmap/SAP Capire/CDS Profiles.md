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

> [!todo] In my understanding profiles don't exist in their own configuration file...
> ...but a profile is simply made up of the entirety of [<profile name>] statements in the manifest.json file.

Profiles are typically defined in a configuration file and activated at runtime using environment variables or [[CLI]] arguments, allowing you to switch configurations without changing the application code.

**Summary**  
[[CDS]] profiles enable flexible management of application configurations, simplifying development, testing, and deployment across different environments.

**Sources**
- [SAP Capire - Configuration Profiles](https://cap.cloud.sap/docs/node.js/cds-env#profiles)