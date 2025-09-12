#Basic #Topic2

TYPE definitions can be declared anywhere in ABAP code. But they are usually declared in the public section of a class or in an interface.
They can be used to define any kind of type: elementary data types, structures, tables or deep types contia
```
TYPE type_name TYPE STANDARD TABLE OF structure WITH EMPTY KEY.

TYPES:
"! Documentation comment
	BEGIN OF ts_structure,
		field1 TYPE matnr,
		field2 TYPE int4,
	END OF ts_structure.
```

TYPE definitions are sometimes called **standalone data types**. This distinguishes them from **bound data types**. A bound data type is created directly with the variable instance using the `DATA` keyword. It cannot be reused and should therefore, not be used.

```abap
DATA my_variable TYPE CHAR LENGTH 20. " don't use this
````

##### ABAP Restful Application Programming Model (RAP)
With ABAP Restful Application Programming Model (RAP), ABAP introduced new specialized ABAP types. These TYPE definitions are references to entities in Business Objects, that are used for transactional behavior.

```abap
TYPE type_name TYPE TABLE FOR CREATE I_EntityView.
```

### Resources
#website [ABAP Cheat Sheets | Data Types and Data Objects](https://github.com/SAP-samples/abap-cheat-sheets/blob/main/16_Data_Types_and_Objects.md)
#website [ABAP Keyword Documentation | TYPES](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENTYPES_STATEMENTS.html)