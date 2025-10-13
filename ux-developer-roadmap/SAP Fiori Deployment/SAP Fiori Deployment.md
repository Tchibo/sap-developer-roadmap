## Deployment

### Deploying Fiori Element Apps
Most Fiori Elements apps are part of Multi-Target Applications (MTAs) projects. A MTA deployment requires connection to an SAP BTP Subaccount with specified organization (ORG) and space (SPACE) to identify the target Cloud Foundry runtime environment. Invoke the build by right-clicking the file mta.yaml. When build is completed right-click the MTA archive file (.mtar) to deploy to Cloud Foundry.

### Deploying Adaptation Projects 
An Adaption project will be deployed to the system where the adapted application resides. In case that you are adapting a SAP Standard ABAP based application in a selected system it is deployed to the ABAP platform of that system. To ensure that the deployment to the ABAP stack of the source system is successful, the necessary details (target: ABAP, destination: where the original app is located, SAP UI5 repository name, package) must first be specified using the Fiori command palette ‘Fiori: Add deployment configuration’. The deployment can then be done using the command palette ‘Fiori: deploy application’.

To avoid all manual steps required for deployment, we are currently working on a SAP Continuous Integration and Delivery scenario.
## Useful Links
- [Build and Deploy Your SAP Fiori App to SAP Business Technology Platform](https://developers.sap.com/tutorials/appstudio-fioriapps-mta-build-deploy..html)
- [Understanding SAP Fiori Launchpad Deployment Options](https://learning.sap.com/learning-journeys/exploring-the-authorization-concept-for-sap-fiori-on-sap-s-4hana/understanding-sap-fiori-launchpad-deployment-options)
- [Deploy the Adaptation Project to the ABAP Repository](https://help.sap.com/docs/bas/developing-sap-fiori-app-in-sap-business-application-studio/deploy-adaptation-project?locale=en-US)
-  [SAP Continuous Integration and Delivery](https://help.sap.com/docs/btp/sap-business-technology-platform/continuous-integration-and-delivery-ci-cd?locale=en-US)
## Community
- [End-to-End Guide: Deploying a Fiori App – From BTP Destination Creation to Public Cloud Deployment](https://community.sap.com/t5/technology-blog-posts-by-members/end-to-end-guide-deploying-a-fiori-app-from-btp-destination-creation-to/ba-p/14038453)
- [SAP Fiori Deployment Options and Recommendations](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-fiori-deployment-options-and-recommendations/ba-p/13351240)



-