#Intermediate 
The CDS Virtual Data Model implements a layered architecture for CDS view entities, creating a systematic stack from database tables to interface, consumption, and projection views. This design approach is an architectural pattern that addresses various concerns of enterprise application development. The layered structure supports separation of concerns, enhances maintainability, promotes reusability, and tailors data representation to different consumption scenarios.

The stack begins with database tables as the raw data persistence layer. On top of this layer are basic interface views, providing a direct representation of database tables with added metadata and initial business semantics. Composite interface views select from basic interface views or other composite interface views and add complexity with associations, compositions, and calculated fields. In the RESTful Application Progamming Model (RAP) composite interface views form the foudation of the business object model. Consumption views, tailored for specific scenarios, add UI annotations and expose only relevant fields. For analytical and transactional queries, projection views take the role of consumption view. 

The layered view entity approach promotes separation of concerns, reusability, and consistency, allowing changes to one layer without affecting the others. It optimizes performance by selecting only necessary fields and records, manages metadata efficiently, and enables granular authorization control. 

## Further reading

#Article [Virtual Data Model and View Types](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/ee6ff9b281d8448f96b4fe6c89f2bdc8/0a875bc7a005465aad92c08becc11776.html?locale=en-US)