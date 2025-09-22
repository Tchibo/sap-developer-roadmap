#Intermediate 
ABAP Core Data Services (CDS) offer different view entity types each serving distinct purposes in the context of crafting virtual data models. View entities extend beyond traditional database views by incorporating metadata, annotations, and specific behaviors. Understanding these types helps with data modeling, particularly within the ABAP RESTful Application Programming Model (RAP).

* ***View Entity**: Serves as a foundational entity for data models, providing SQL-like definitions for field selection, joins, and conditions, transforming technical fields into business-friendly names. The **basic** view entity selects data from database tables, **interface** view entities select data from basic view entities or other interface view entities. Value helps are realized as view entities enhancing search functionality for a better user experience in Fiori UIs.

* ***Root View Entity**: Acts as a top-level business object entry point, establishing compositions and associations, enabling transactional behavior and draft handling.

* ***Projection View Entity**: Specializes existing entities for analytical or transactional use cases in business applications, adding UI annotations, reducing the field list, and facilitating direct OData service exposure. Projection view entities are special use cases of consumption views, serving the purpose of transactional or analytical queries.

* ***Custom Entity**: Integrates external data sources within CDS that cannot be handled by SQL access to the underlying database, enabling complex retrieval logic through ABAP code.

* **Table function**: Uses HANA SQLScript in an ABAP Managed Database Procedure (AMDP) to access data. Table functions are good for accessing HANA native functions from CDS or when performance is of utmost importance.

## Further reading

#Article Entity Modeling](https://help.sap.com/docs/abap-cloud/abap-data-models/entity-modeling)