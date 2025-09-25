---
tags:
  - sap-btp
  - security
  - basic
links:
  - "[[SAP BTP]]"
  - "[[Security]]"
source:
aliases:
---
Roles in [[SAP BTP|SAP Business Technology Platform]] are used to control access and enforce restrictions within applications and services. By assigning roles, you can specify which actions or features are available to different user groups. Roles can be granted to users directly or through role collections, allowing for flexible and fine-grained access management. This ensures that only authorized users can perform sensitive operations or access restricted data within the application or service.

Roles are typically defined and managed in the [[SAP BTP Cockpit]], where administrators can assign them to users or groups according to business requirements. In addition to roles and role collections, attributes play an important part in personalizing authorization. Attributes allow administrators to refine access down to row level and ensure that users can only view or modify data relevant to their organizational context. For example, authorizations can be checked on the level of a sales organization or company code, providing more precise control within business scenarios.

**Sources**
- [SAP BTP - Working with Roles](https://help.sap.com/docs/cloud-portal-service/sap-cloud-portal-service-for-neo-environment/working-with-roles?locale=en-US)
- [SAP BTP - Roles and Role-Collections](https://help.sap.com/docs/btp/sap-business-technology-platform/roles-and-role-collections)