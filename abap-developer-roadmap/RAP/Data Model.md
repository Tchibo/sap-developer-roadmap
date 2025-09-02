#basic

The RAP data model is built on the CDS data model and consists of several layers:

- **Database table**: The foundation layer containing the actual data
- **Interface view**: The core component defining all fields and relationships of a RAP business object

> [!todo] Behaviour projection vs entity projection
> The interface view entity does not include 'behaviours' as it is just the data model. Behaviours come from the behaviour definition which itself is projected in the behaviour projection.

- **Projection view**: Built on top of the interface view, tailored for specific use cases (such as Fiori UI). It contains a subset of fields and behaviors from the interface view, determining what capabilities are available for that particular use case. Multiple projection views can reference the same interface view.

> [!todo] Service definition and service binding as separate subtopics
> Service definition and service binding deserve to be separate sub-topics as the mention here is short compared to the role the play in the RAP repository object stack.

A RAP business object may include multiple entities (root and child entities) organized in a hierarchical structure. This structure is exposed through a service definition and service binding that specifies the technology (OData V2, V4).
## Resources
- [Business Object Projection](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/6e7a10d30b74412a9482a80b0b88e005.html?locale=en-US)