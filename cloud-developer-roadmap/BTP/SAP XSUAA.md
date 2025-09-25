---
tags:
  - sap-btp
  - security
links:
  - "[[Security]]"
source:
aliases:
  - XSUAA
---
The SAP XSUAA is the central component for managing authentication and authorization in applications running on [[SAP BTP]] in the [[Cloud Foundry]] environment. It serves as an [[OAuth 2.0]]–compliant authorization server that issues JSON Web Tokens ([[JWT]]s) to ensure secure access to services. While XSUAA itself does not store user accounts, it delegates authentication to trusted identity providers such as the [[SAP Identity Authentication Service]] or corporate [[IdP]]s.

In [[SAP Capire]] applications, [[Roles|roles]] and [[Role-Collections|role-collections]] are defined in the `xs-security.json` file. This configuration includes the application name (`xsappname`), defined scopes and role templates. Developers deploy this configuration by creating an XSUAA service instance and binding it to the application. To authenticate users and handle routing, the [[App Router]] is required. SAP recommends using the [[Managed App Router]], which can be created directly from the MTA editor in [[SAP Build Code]]. This approach simplifies setup, reduces maintenance overhead, and ensures that security configurations such as XSUAA integration are managed consistently by the platform.

**Sources**
- [SAP Help Portal - SAP BTP XS Advanced UAA (Cloud Foundry)](https://help.sap.com/docs/cloud-identity-services/cloud-identity-services/sap-btp-xs-advanced-uaa-cloud-foundry?locale=en-US)
- [SAP Community - Demystifying XSUAA in SAP Cloud Foundry]([Demystifying XSUAA in SAP Cloud Foundry](https://community.sap.com/t5/technology-blog-posts-by-sap/demystifying-xsuaa-in-sap-cloud-foundry/ba-p/13468237))
- [SAP Cloud SDK - SAP BTP, Cloud Foundry Environment XSUAA Explained](https://sap.github.io/cloud-sdk/docs/java/guides/cloud-foundry-xsuaa-service)
- [SAP Discovery Center - SAP Authorization and Trust Management Service](https://discovery-center.cloud.sap/serviceCatalog/authorization-and-trust-management-service?region=all)
- [SAP Capire - Role Assignments with XSUAA](https://cap.cloud.sap/docs/guides/security/authorization#xsuaa-configuration)