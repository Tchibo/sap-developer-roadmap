## 1. Basics

- SAP landscape architecture
	- https://community.sap.com/t5/technology-blog-posts-by-members/sap-integration-architecture-guide/ba-p/13955539
		- ISA-M
- Destinations
- SAP Accelerator Hub --> Link
## 2. Platform Topics
	Authentication & authorization mechanisms?? --> Link zu ??
		- Basic, OAuth 2.0 (application-to-application), Principal Propagation (user-to-application)
	Cloud Connector
	Connectivity Service
	XSUAA
	
## 3. Data Integration
	-SLT, SDA,...

## 4. **Process Integration

- Integration flow designs
- Adapters (erwähnen --> Link Doku)
	- SOAP, REST, IDoc, SFTP, Mail, etc.
- Message mapping and transformation
- Content modifiers and headers
- Error handling and monitoring
- Groovy/JavaScript scripting
- Security artifacts management (OAuth,...)
- API types 
	- IDoc, RFC, BAPI, SOAP, REST, OData -> verlinken zu Fiori/ABAP Roadmap 
	- synchron, asynchron, push, pull, pubsub,...
- Message protocols and formats 
	- XML, JSON

## 5. **API Management**

- Introduction
    - based on apigee - link to documentation
    - limited to OData, REST, SOAP
    - exposes APIs (one-to-many)

- Flows and Policies
    - Preflow, Postflow, Conditional Flow
        
        - [https://community.sap.com/t5/technology-blog-posts-by-sap/sap-api-management-understanding-policy-flow/ba-p/13187144](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-api-management-understanding-policy-flow/ba-p/13187144)
            
- API Hub
    - OpenAPI Specifications

## 6. Event Mesh / AEM

- Differences between EM and AEM (nur AEM?)
- EDA (Event Driven Architecture)
- EEE (Enterprise Event Enablement) 
- Event Format (Data Events, Notification Events)
- Event Schema
- AEM Designer and AEM Broker
- Dead Messages
## 7. **Monitoring & Operations**

- Message monitoring
- Error resolution
- Performance optimization
- Logging and tracing
- Transport management
- CALM
