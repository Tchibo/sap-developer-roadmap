#Medium 
The Behavior Definition Language (BDL) in SAP’s RESTful Application Programming Model defines the runtime behavior of business objects declaratively. Any operation declared in BDL must also be implemented as a method in the associated ABAP behavior pool class. A single BDL file defines a whole business object, including its root entity and all child entities.
#### Types of Behavior

RAP entities support different operation types:

- **Operations**: Basic CRUD actions (Create, Read, Update, Delete) automatically handled by the framework in managed scenarios.
- **Draft operations**: Enable immediate storage of user input, managed automatically by the framework in managed scenarios.
- **Validations** and **Determinations**: Ensure data consistency within the RAP business object.
- **Actions**: Custom business operations specific to the entity.
- **Feature and authorization control** to enable or disable operations.
- Automatic **UUID generation** (numbering : managed) 
- Making field read-only or mandatory
- Defining an **e-tag** for optimistic locking in draft creation
- Declaring **side effects** when a user input or action requires a related action to be triggered.


```BDL
managed implementation in class bp_demo_rap_foreign_entity unique;

define behavior for DEMO_RAP_FOREIGN_ENTITY alias RootEntity
persistent table DEMO_DBTAB_ROOT
lock master
...
{
  create;
  update;
  delete;

  field(readonly:update) key_field;
}
```

## Further reading

#website [RAP - Behavior Definitions | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENCDS_BDEF.html)
#website [RAP BDL - Feature Tables | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENRAP_FEATURE_TABLE.html)