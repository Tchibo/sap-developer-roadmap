#Basic #Topic3

The RAP data model is built on the CDS data model and consists of several layers:

- **Database table**: The foundation layer containing the actual data
- **Interface view**: The core component that defines all fields and associations of a RAP business object. Its paired behavior definition enumerates all operations that can be performed on this business object.

- **Projection view**: Built atop the interface view and tailored to specific scenarios (e.g., Fiori UI). It exposes a subset of fields from the interface view, and the paired projection behavior definition specifies which capabilities are available for that scenario. Multiple projection views can reference the same interface view.

A RAP business object may include multiple entities (root and child entities) organized in a hierarchical structure. This structure is exposed through a service definition and service binding that specifies the technology (OData V2, V4).
## Resources
- [Business Object Projection](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/6e7a10d30b74412a9482a80b0b88e005.html?locale=en-US)