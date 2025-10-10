---
tags:
  - sap-capire
  - basic
links:
  - "[[Introduction 2 CAP]]"
  - "[[SAP Capire|SAP Capire]]"
source:
aliases:
---
> [!NOTE] What do I need to know before initializing the project?
> - Install **[[Node.js]]** and **[[NPM]]**
> - Have a basic understanding of **[[CDS]]** modeling
> - Install the [[SAP Capire|CAP]] CLI globally: `npm install -g @sap/cds`

To start a [[SAP Capire]] project, ensure you have [[Node.js]], [[NPM]], and the [[cds CLI]] installed, along with a basic understanding of [[CDS]] modeling.

**Project Initialization**  
Initialize a new project with:
```bash
cds init my-cap-project
cd my-cap-project
npm install
```

**Project Structure**  
The project structure includes:
- `db/`: Database layer with [[CDS]] models.
- `srv/`: Service definitions and business logic.
- `app/`: User interface layer, often using [[Fiori Elements]].
- `i18n/`: Localization files.
- `test/`: Automated tests.
- `package.json`: Project configuration.

This layered structure helps manage complex applications by separating concerns for the database, services, UI, and testing, following best practices for SAP cloud development.

**Summary**  
Before starting, install [[Node.js]], [[NPM]], and the [[cds CLI]], and understand [[CDS]] modeling. The project structure is organized into layers for database, services, UI, localization, and testing, which supports efficient application management.

**Sources**
- [SAP Capire - Getting started](https://cap.cloud.sap/docs/get-started/#getting-started)
- [SAP Capire - Jumpstarting Projects](https://cap.cloud.sap/docs/about/#jumpstarting-projects)