---
tags:
  - build
  - deployment
links:
source:
aliases:
---
In [[SAP Capire]], building an MTA-based project involves generating deployment artifacts, compiling user interfaces, and packaging the application for [[SAP BTP]]. Use `cds build` to compile services into the `gen` directory. The `--clean` flag removes outdated files before the build. For developers preferring a graphical interface, SAP Build Code allows starting the build via the context menu on the `mta.yaml` file.

User interfaces in the `app` folder are built with `npm run build`, producing a `dist` folder containing the deployable UI. The `mta.yaml` file defines the structure of the application, including modules, resources, and dependencies on [[SAP BTP]] services, and acts as the blueprint for deployment. To package the project into a deployment-ready `.mtar` archive, run `mbt build`, which reads the `mta.yaml` and includes all modules.

**Summary**  
A [[SAP Capire]] Node.js project is built by compiling services with `cds build`, building UIs with `npm run build`, and defining the application structure in `mta.yaml`. The `mbt build` command creates a deployable MTA archive for [[SAP BTP]], with the option to trigger builds either via the CLI or SAP Build Code’s context menu.

**Sources**

- [SAP Capire - Troubleshooting MTA](https://cap.cloud.sap/docs/get-started/troubleshooting#mta)
    
- [SAP Help Portal - Multitarget Applications in Cloud Foundry Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/multitarget-applications-in-cloud-foundry-environment?locale=en-US)
    
- [SAP Capire - Customizing `cds build`](https://cap.cloud.sap/docs/guides/deployment/custom-builds#customizing-cds-build)