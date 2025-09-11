---
tags:
  - "#rework"
  - deployment
  - intermediate
links:
source:
aliases:
---
> [!IMPORTANT] Disclaimer
> This post focuses on deploying an MTA archive to an SAP BTP Cloud Foundry environment.

> [!toDo] First explain the concept of a 'Multi-target Application'
> ...and the fact that its micro-services defined and required are described in the mta.yaml. That the microservices defined and required are created on the BTP runtime at time of deployment. That a BTP sub account, organization and space need to be connected at time of deployment as it identifies the Cloud Foundry runtime that the MTA should run on. That microservices of an MTA share credentials with each other through service binding. Thus creating conceptual understanding before going into the operational functioning of deployment.

After generating the MTAR archive of your [[SAP Capire]] project, deploy it to the target [[SAP BTP Subaccount]] using the [[cf CLI]]. First, log in to the subaccount:

```bash
cf login -t https://api.cf.<REGION>.hana.ondemand.com -u <USERNAME> -o <ORG> -s <SPACE>
```
You can use your password with the `-p` flag or single sign-on with `--sso`.

Once authenticated, deploy the MTAR archive:
```bash
cf deploy PATH_TO_YOUR_MTAR_ARCHIVE -f
```
The `-f` flag forces deployment without confirmation. The process duration depends on the MTAR size, number of services, and database. During deployment, the archive is unpacked, application modules are pushed to Cloud Foundry, and service instances from the `mta.yaml` are created or updated.

**Sources**
- [SAP Capire - Deployment](https://cap.cloud.sap/docs/guides/deployment/#deployment)
- [SAP Capire - Deploy to Cloud Foundry](https://cap.cloud.sap/docs/guides/deployment/to-cf)
- [SAP Learning - Deploy your First Multitarget Application](https://developers.sap.com/tutorials/btp-cf-deploy-mta..html)
- [Cloud MTA Build Tool](https://sap.github.io/cloud-mta-build-tool/)
- [Cloud Foundry - CLI](https://docs.cloudfoundry.org/cf-cli/install-go-cli.html)