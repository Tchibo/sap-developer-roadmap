#Intermediate 
The behavior implementation (an ABAP behavior pool class) implements operations declared in the behavior definition (BDL). It executes whenever the RAP business object is accessed, whether from a Fiori app, OData web service, or ABAP code.

##### Entity Manipulation Language
SAP created Entity Manipulation Language (EML) as a SQL-like language to access RAP business objects from ABAP. EML ensures only allowed operations execute and required validations trigger. And it respects the hierarchical structure: child entities are manipulated via the root entity.

##### TYPES
RAP provides ABAP types for operations (read, create, update, delete) and message handling (reported, failed). These types can be defined in the behavior pool for reuse and as method parameters to modularize code.

##### Message and Error Handling
Each action implementation receives reported and failed structures. Use reported to send messages to users - they display automatically in the UI based on type (info, warning, error). Best practice is using MESSAGE INTO and filling reported from SY to maintain where-used functionality.

Fill failed when operations fail. This triggers automatic rollback to restore the last consistent state.

#### Resources
#website  [ABAP Behavior Pools (ABP) | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENABAP_BEHAVIOR_POOLS.html)
#website [Entity Manipulation Language (EML) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/af7782de6b9140e29a24eae607bf4138.html?locale=en-US)
