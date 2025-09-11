---
tags:
  - tool
  - advanced
links:
source:
aliases:
  - cds plugins
  - cds plugin
  - CDS Plugin
---
> [!todo] Outline the difference between CDS Plugin and what happens with the 'cds add' command
> Do clarify whether there is a difference between a CDS plugin with its cds-plugin.js file as outlined here and running the 'cds --add <feature>' command. Or if it is in fact the same.

Plugins are a proven software concept: small programs that attach (“plug in”) to enhance existing functionality. Within the [[SAP Capire]] Framework, CDS Plugins empower developers to extend [[SAP Capire|CAP]]’s standard workflows or introduce new features such as file attachment handling even when built-in support is not available.

The [[SAP Capire|CAP]] ecosystem already offers a rich collection of CDS plugins maintained by SAP and the community, covering functionalities like file attachments, [[WebSocket]], [[GraphQL]] adapters, [[audit logging]], [[change tracking]] and many more...

On the architecture side, [[SAP Capire|CAP]] [[Node.js]] supports these plugins through the “cds-plugin” mechanism. Each plugin typically consists of:
- A **cds-plugin.js** file detected automatically in `Node.js` projects and loaded during `cds serve`, `cds build`, and related `CLI` commands.
- Optional configuration in **package.json**, using the `cds` section for auto-configuration of services like databases.
This setup enables effortless plug‑and‑play experiences just install a plugin (e.g. `@cap-js/attachments`), add model annotations (e.g. `using { Attachments }`), then `cds watch` to activate it.

**Summary**
SAP Capire provides the posibility to implement CDS Plugins to extend standard workflows or implement new features. The framework provides:
- Ready-to-use prebuilt plugins (e.g., attachments, [[WebSocket]], [[GraphQL]], audit logging) 
- Automatic integration via **cds-plugin.js** and `cds` config in package.json 
- Seamless use in [[SAP Capire|CAP]] [[Node.js]] through `cds serve`, `cds build`, etc.

This makes extending and enhancing [[SAP Capire|CAP]] applications fast and modular.

**Sources**
- [SAP Capire - CDS Plugin Packages](https://cap.cloud.sap/docs/node.js/cds-plugins)
- [SAP Capire - CAP Plugins & Enhancements](https://cap.cloud.sap/docs/plugins/#cap-plugins-enhancements)
- [Best of cap-js - List of Plugins](https://bestofcapjs.org/)
- [SAP Capire - Demo Plugin - Postgres Build Plugin](https://cap.cloud.sap/docs/plugins/#cap-plugins-enhancements) 
- [SAP Capire - Plugins for `cds add`](https://cap.cloud.sap/docs/tools/apis/cds-add#don-t-do-too-much-work-in-cds-add)