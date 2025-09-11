---
tags:
  - cli
  - tool
  - sap
  - cloud-foundry
links:
  - "[[SAP Capire|SAP Capire]]"
source: https://docs.cloudfoundry.org/cf-cli/
aliases:
---
The [[Cloud Foundry]] [[CLI]] (`cf` [[CLI]]) is a command-line interface for interacting with [[Cloud Foundry]] environments, allowing developers to deploy, manage, and scale applications.

**Key Features:**
- **Application Deployment:** Push applications using various buildpacks.
- **Service Management:** Create, bind, and manage services like databases and caches.
- **Application Management:** Start, stop, restage, and scale applications, with real-time monitoring and logging.
- **User and Role Management:** Manage user accounts and permissions.
- **Space and Org Management:** Organize resources and teams.
- **Plugin Support:** Extend functionality with custom plugins.

In SAP environments, particularly on the [[SAP BTP]], the `cf` [[CLI]] is used to manage applications and services within SAP's [[Cloud Foundry]] infrastructure.

> [!todo] Preinstalled in SAP Build Code
> Do mention the fact that it comes preinstalled when using SAP Build Code. Separate installation required when working locally in VS Code only.

The `cf` [[CLI]] can be installed on [[Windows]], [[macOS]], and [[Linux]].

**Summary**
The `cf` [[CLI]] is a vital tool for managing applications in [[Cloud Foundry]] environments, including [[SAP BTP]]. It supports the full application lifecycle, service integration, and user management. Its plugin system allows for extensibility.