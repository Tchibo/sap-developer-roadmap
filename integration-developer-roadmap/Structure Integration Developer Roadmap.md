## 1. Basics

- SAP landscape architecture
	- https://community.sap.com/t5/technology-blog-posts-by-members/sap-integration-architecture-guide/ba-p/13955539
- API types 
	- IDoc, RFC, BAPI, SOAP, REST, OData -> verlinken zu Fiori/ABAP Roadmap 
	- synchron, asynchron, push, pull,...
- Message protocols and formats 
	- XML, JSON
- Authentication & authorization mechanisms?? --> Link zu ??
	- Basic, OAuth 2.0 (application-to-application), Principal Propagation (user-to-application)
- Destinations
- - Groovy/JavaScript scripting
- SAP Accelerator Hub --> Link

## 2. **SAP Integration Suite 

- Integration flow designs
- Adapters 
	- SOAP, REST, IDoc, SFTP, Mail, etc.
- Message mapping and transformation
- Content modifiers and headers
- Error handling and monitoring
- Security artifacts management (OAuth,...)

## 3. **API Management**

- Introduction
    - based on apigee - link to documentation
    - limited to OData, REST, SOAP
    - exposes APIs (one-to-many)

- Flows and Policies
    - Preflow, Postflow, Conditional Flow
        
        - [https://community.sap.com/t5/technology-blog-posts-by-sap/sap-api-management-understanding-policy-flow/ba-p/13187144](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-api-management-understanding-policy-flow/ba-p/13187144)
            
        - [https://help.sap.com/docs/sap-api-management/sap-api-management-for-neo-environment/flow?locale=en-US&q=defaultfaultflow](https://help.sap.com/docs/sap-api-management/sap-api-management-for-neo-environment/flow?locale=en-US&q=defaultfaultflow)
            
- API Hub
    - OpenAPI Specifications

## 4. Event Mesh / AEM

- Differences between EM and AEM 
- EDA (Event Driven Architecture)
- EEE (Enterprise Event Enablement) 
- Event Format (Data Events, Notification Events)
- Event Schema
- AEM Designer and AEM Broker
- Dead Messages
## 5. **Monitoring & Operations**

- Message monitoring
- Error resolution
- Performance optimization
- Logging and tracing
- Transport management
- CALM
