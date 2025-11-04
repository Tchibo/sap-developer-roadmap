---
tags:
  - security
  - sap-btp
  - intermediate
links:
source:
aliases:
  - Application Router
---
The SAP Application Router (Approuter) is a [[Node.js]]-based library that serves as the central access point for applications running on SAP [[SAP BTP|Business Technology Platform]]. It is responsible for handling authentication and authorization, serving static resources, rewriting URLs, and forwarding requests to backend services or microservices while preserving user identity. The Approuter simplifies the integration of various services by acting as an intermediary that manages connectivity and security. Detailed information about its capabilities, configuration options, service bindings, and deployment steps can be found in the [NPMJS Readme](https://www.npmjs.com/package/@sap/approuter?activeTab=readme) of the service.

**Summary**
The SAP Approuter is a [[Node.js]]-based component that acts as the central entry point to an enterprise application. It handles the delivery of static content, manages user authentication, performs URL rewriting, and routes or proxies incoming requests to backend microservices while forwarding user context.

**Sources**
- [SAP Help Portal - Application Router](https://help.sap.com/docs/btp/sap-business-technology-platform/application-router?locale=en-US)
- [NPMJS - @sap/approuter](https://www.npmjs.com/package/@sap/approuter?activeTab=readme)
- [SAP Community - SAP Application Router](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-application-router/ba-p/13393550)
- [SAP Community - What is SAP Approuter and its importance?](https://community.sap.com/t5/technology-blog-posts-by-members/what-is-sap-approuter-and-its-importance/ba-p/13797947)
- [SAP Capire - Configuring App Router](https://cap.cloud.sap/docs/guides/extensibility/customization#app-router)