---
tags:
  - security
  - cap-cds
  - basic
links:
source:
aliases:
---
Within the service definition of the [[SAP Capire]] Framework, it is possible to restrict access to specific services, tables, and records. Access control can be enforced based on authentication status, user groups, user attributes (including feature toggles for selected users), or even more complex conditions such as the user’s country of origin.

Additionally, you can implement further authorization checks within the business logic of a service, using event handlers to perform validations based on user roles or attributes.

The [[SAP Capire]] Framework offers multiple tools to define these restrictions: you can use the [[CDS]] annotation `@restrict` for declarative access control or implement custom logic within event handlers to meet more advanced requirements.

**Summary**  
The [[SAP Capire]] Framework provides several mechanisms for adding restrictions on tables or individual records. Access control can be managed using the [[CDS]] `@restrict` annotation or implemented programmatically within event handlers.

**Sources**
- [SAP Capire - User-Claims](https://cap.cloud.sap/docs/guides/security/authorization#user-claims)
- [SAP Capire - Restrictions](https://cap.cloud.sap/docs/guides/security/authorization#restrictions)
- [SAP Capire - Instance-Based Authorization](https://cap.cloud.sap/docs/guides/security/authorization#user-claims)