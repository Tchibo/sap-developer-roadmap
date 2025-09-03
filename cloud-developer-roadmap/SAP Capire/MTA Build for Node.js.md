---
tags:
  - build
  - deployment
links:
source:
aliases:
---
> [!IMPORTANT] Disclaimer  
> This guide focuses on building an MTA-based project.

Use `cds build` to generate deployment artifacts in the `gen` directory. The `--clean` flag removes outdated files before the build.

User interfaces in the `app` folder are built with `npm run build`, creating a `dist` folder with the deployable UI.

The `mta.yaml` file describes the application structure, defining modules, resources, and dependencies on [[SAP BTP]] services. It serves as the deployment blueprint.

To create the deployment archive, run `mbt build`, which reads the `mta.yaml` and packages all modules into a `.mtar` file. This file is used for deployment to [[SAP BTP]].

**Summary**
A [[SAP Capire]] project with [[Node.js]] is built by compiling services with `cds build`, building UIs with `npm run build`, and configuring the application with `mta.yaml`. The `mbt build` command creates an MTA archive for deployment.

**Sources**
- [SAP Capire - Troubleshooting MTA](https://cap.cloud.sap/docs/get-started/troubleshooting#mta)
- [SAP Help Portal - Multitarget Applications in the Cloud Foundry Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/multitarget-applications-in-cloud-foundry-environment?locale=en-US)
- [SAP Capire - Customizing `cds build`](https://cap.cloud.sap/docs/guides/deployment/custom-builds#customizing-cds-build)