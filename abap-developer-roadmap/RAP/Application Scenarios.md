#Intermediate #Topic4

The RAP framework can be used for different scenarios and constellations:

- **Read-only application** do not require any RAP artifacts and are solely based on CDS objects, a service definition and service binding. 
- **Transactional applications**: In an application with CRUD operations, RAP's managed features are most helpful. 
- **UI application**: With RAP, a UI can be declared by annotations only.
- **Web service**: When no UI is needed, RAP applications can be accessed as web service (e.g. OData V4).
- **Managed scenario**: In managed RAP, CRUD operations are provided by the RAP framework. 
- **Unmanaged scenario**: In unmanaged RAP, CUD operations must be implemented. This is mostly used to integrate and re-used existing coding.
- SAP recommends to use **OData V4** for transactional apps. But there are other types available too.
## Resources
- [Develop](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/ffef7e02127e442793f24e3dc902c824.html?locale=en-US)
- [Managed vs Unmanaged](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/e11757cf7e664121b9f583e7ca0eeb39.html?locale=en-US)
- [Service Binding](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/b58a3c27df4e406f9335d4b346f6be04.html?locale=en-US)