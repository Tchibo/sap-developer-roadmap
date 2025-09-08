SAP created Entity Manipulation Language (EML) as a SQL-like language to access RAP business objects from ABAP. EML ensures only allowed operations execute and required validations trigger. And it respects the hierarchical structure: child entities are manipulated via the root entity.
```
MODIFY ENTITIES OF R_SalesOrderTP
	ENTITY Order UPDATE FROM lt_orders_updated
	REPORTED FINAL(ls_reported) FAILED FINAL(ls_failed).
```

##### TYPES
RAP provides ABAP types for operations (read, create, update, delete) and message handling (reported, failed). These types are derived from the underlying CDS entities. They contain the entities’ fields as well as generated RAP structures (for example, `%key` , which contains all key fields) to aid RAP operations.
Derived types can be defined in pool class definitions for reuse and as method parameters to modularize code.
```
DATA orders_updated TYPE TABLE FOR UPDATE R_SalesOrderTP\\Order.
```

##### Message and Error Handling
Each action implementation receives reported and failed structures. Use reported to send messages to users - they display automatically in the UI based on type (info, warning, error). Best practice is using MESSAGE INTO and filling reported from SY to maintain where-used functionality. But this requires custom implementation.

Fill failed when operations fail. This triggers automatic rollback to restore the last consistent state.
```
MESSAGE e041(message_class) INTO DATA(lv_message).
APPEND VALUE #(  %msg = 
	new_message_with_text( text     = lv_message
						   severity = if_abap_behv_message=>severity-error 
					      ) ) TO reported-Order.
```

#### Resources
- #website [Entity Manipulation Language (EML) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/af7782de6b9140e29a24eae607bf4138.html?locale=en-US)
- #website [Derived Data Types | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/5a32ad145caa42c4bc14c18402f95d90.html?locale=en-US)
- #website [Components of BDEF Derived Types | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/abapderived_types_comp.html)
- #website [Messages | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/ac74189b5cae49c1b091f04393bac069.html?locale=en-US)
 