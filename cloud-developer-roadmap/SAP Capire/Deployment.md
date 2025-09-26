---
tags:
  - "#rework"
  - deployment
  - intermediate
links:
source:
aliases:
---
Before deploying an [[SAP Capire|CAP]] project to [[SAP BTP]], it is important to understand the concept of a Multi-Target Application (MTA). An MTA is a package that bundles multiple interconnected components, such as microservices, UI modules, and resource definitions, into a single deployable archive. The `mta.yaml` file describes these components, their dependencies, and required services. During deployment, the microservices defined in the MTA are created or updated on the target [[SAP BTP|BTP]] runtime. Components of the MTA share credentials through service bindings, enabling secure communication between services.

To deploy an MTA, a connection to a [[SAP BTP Subaccount]] is required. You must specify the organization (`ORG`) and space (`SPACE`) within the subaccount, which identifies the Cloud Foundry runtime where the application should run. This ensures that all services and modules of the MTA are deployed to the correct environment.

After generating the MTAR archive of your project using `mbt build`, deploy it to the target subaccount using the [[cf CLI]]:
```bash
cf login -t https://api.cf.<REGION>.hana.ondemand.com -u <USERNAME> -o <ORG> -s <SPACE>
```

You can authenticate using a password with the `-p` flag or single sign-on with `--sso`. Once logged in, deploy the MTAR archive:
```bash
cf deploy PATH_TO_YOUR_MTAR_ARCHIVE -f
```

The `-f` flag forces deployment without confirmation. Deployment duration depends on the archive size, the number of services, and the database configuration. During deployment, the MTAR archive is unpacked, application modules are pushed to Cloud Foundry, and service instances defined in `mta.yaml` are created or updated automatically.

Understanding the MTA concept, service bindings, and the need for a connected subaccount, organization, and space provides a clear conceptual foundation before performing operational deployment steps.

**Sources**
- [SAP Capire - Deployment](https://cap.cloud.sap/docs/guides/deployment/#deployment)
- [SAP Capire - Deploy to Cloud Foundry](https://cap.cloud.sap/docs/guides/deployment/to-cf)
- [SAP Learning - Deploy your First Multitarget Application](https://developers.sap.com/tutorials/btp-cf-deploy-mta..html)
- [Cloud MTA Build Tool](https://sap.github.io/cloud-mta-build-tool/)
- [Cloud Foundry - CLI](https://docs.cloudfoundry.org/cf-cli/install-go-cli.html)