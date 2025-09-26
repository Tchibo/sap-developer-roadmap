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
Plugins are a proven software concept: small programs that attach (“plug in”) to enhance existing functionality. Within the [[SAP Capire]] Framework, CDS Plugins empower developers to extend [[SAP Capire|CAP]]’s standard workflows or introduce new features such as file attachment handling even when built-in support is not available.

The [[SAP Capire|CAP]] ecosystem already offers a rich collection of CDS plugins maintained by SAP and the community, covering functionalities like file attachments, [[WebSocket]], [[GraphQL]] adapters, [[audit logging]], [[change tracking]] and many more...

On the architecture side, [[SAP Capire|CAP]] [[Node.js]] supports these plugins through the “cds-plugin” mechanism. Each plugin typically consists of:
- A **cds-plugin.js** file detected automatically in `Node.js` projects and loaded during `cds serve`, `cds build`, and related `CLI` commands.
- Optional configuration in **package.json**, using the `cds` section for auto-configuration of services like databases.
This setup enables effortless plug‑and‑play experiences just install a plugin (e.g. `@cap-js/attachments`), add model annotations (e.g. `using { Attachments }`), then `cds watch` to activate it.

**Sources**
- [SAP Capire - CDS Plugin Packages](https://cap.cloud.sap/docs/node.js/cds-plugins)
- [SAP Capire - CAP Plugins & Enhancements](https://cap.cloud.sap/docs/plugins/#cap-plugins-enhancements)
- [Best of cap-js - List of Plugins](https://bestofcapjs.org/)
- [SAP Capire - Demo Plugin - Postgres Build Plugin](https://cap.cloud.sap/docs/plugins/#cap-plugins-enhancements) 
- [SAP Capire - Plugins for `cds add`](https://cap.cloud.sap/docs/tools/apis/cds-add#don-t-do-too-much-work-in-cds-add)