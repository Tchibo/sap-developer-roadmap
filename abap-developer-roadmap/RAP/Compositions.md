Core Data Services (CDS) compositions are a special type of association that enable developers to model entity relations that reflect parent-child relationships. In a composition, child entities cannot exist independently of their parent. For instance, a Sales Order line item cannot exist without the Sales Order header object.

**Key characteristics of compositions**
- Operations cascade from parent to child (create, update, delete). For example, child entities are automatically deleted when the parent is removed.
- Changes to parent and child entities occur within the same transaction, ensuring data consistency.

> [!todo] Please check code snipped
> - [x] In reference to I_SalesOrder I suggest a I_SalesOrder Item composition. You could look at I_SalesOrderTP to see how they do the composition from order to item.
> 	- [x] Good point. I chose R_SalesOrderTP because it defines the composition relationships.

```DDL
define root view entity R_SalesOrderTP as select from I_SalesOrder

//child associations
composition [0..*] of R_SalesOrderItemTP as _Item
```

```DDL
// child entity
define view entity R_SalesOrderItemTP as select from I_SalesOrderItem

association to parent R_SalesOrderTP as _SalesOrder on $projection.SalesOrder = _SalesOrder.SalesOrder
```
Compositions serve as the foundation for creating business objects and are essential for implementing business objects in the RESTful Application Programming Model (RAP). 


## Further reading

#Article [Compositions](https://help.sap.com/docs/abap-cloud/abap-data-models/cds-compositions)