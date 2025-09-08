> [!todo] Naming 'behaviour pool'
> - [ ] Here and in other sections of the RAP topic please use 'behaviour pool' instead of 'behaviour pool class'. The the behaviour implementation class is a 'class pool'. 
> 	- [ ] Switched to 'behavior class pool'. I'd like to mention 'class'.

The Behavior Definition Language (BDL) in SAP’s RESTful Application Programming Model defines the runtime behavior of business objects declaratively. Any operation declared in BDL must also be implemented as a method in the associated ABAP behavior class pool. A single BDL file defines a whole business object, including its root entity and all child entities.
#### Types of Behavior

> [!todo] 'Operation types'
> - [ ] Making a field read-only or mandatory is static feature control, i.e. 'Making field read only or mandatory' could be used to explain list item 'Feature and authorization control'
> 	- [ ] Not sure what you intend here? Do you want me to create new text for 'Feature and authorization control'? 
> 	- [ ] Removed 'Making field read only or mandatory' 

RAP entities support different operation types:

- **Operations**: Basic CRUD actions (Create, Read, Update, Delete) automatically handled by the framework in managed scenarios.
- **Draft operations**: Enable immediate storage of user input, managed automatically by the framework in managed scenarios.
- **Validations** and **Determinations**: Ensure data consistency within the RAP business object.
- **Actions**: Custom business operations specific to the entity.
- **Feature and authorization control** to enable or disable operations.
- Automatic **UUID generation** (`numbering : managed`) 
- Defining an **e-tag** for optimistic locking in draft creation
- Declaring **side effects** when a user input or action requires a related action to be triggered.


```BDL
managed implementation in class bp_demo_rap_foreign_entity unique;

define behavior for DEMO_RAP_FOREIGN_ENTITY alias RootEntity
persistent table DEMO_DBTAB_ROOT
lock master
etag master ChangedAt
...
{
  field ( numbering : managed ) Id;
  
  create;
  update;
  delete;
  
  validation checkField on save { create; }
  action startProcess parameter I_startProcessInput result [1] $self;
}
```

## Further reading

#website [RAP - Behavior Definitions | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENCDS_BDEF.html)
#website [RAP BDL - Feature Tables | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENRAP_FEATURE_TABLE.html)