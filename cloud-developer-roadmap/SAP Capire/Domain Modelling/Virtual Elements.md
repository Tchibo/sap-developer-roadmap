---
tags:
  - cap-cds
  - data-modelling
  - cds
  - intermediate
links:
  - "[[Domain Modelling]]"
  - "[[Domain Entites]]"
  - "[[Views & Projections]]"
source: https://cap.cloud.sap/docs/cds/cdl#virtual-elements
aliases:
---
Virtual elements in [[SAP Capire]] are defined by using the `virtual` keyword before an element in an entity. These elements are part of the data model and are included in the [[OData]] metadata, but they are not stored in the database. Instead, virtual elements are calculated or filled at runtime, such as by handlers or through service logic. This makes them useful for exposing computed fields or transient values without altering the persistent storage schema.

**Example**
```cds
entity Employees {
  key ID         : UUID;
      name       : String;
      virtual something : String(11);
}
```

In this example, the field `something` is a virtual element and will appear in the service metadata but will not be physically stored in the database.

**Summary**  
Virtual elements in [[SAP Capire]] are non-persistent fields defined in the data model. They appear in service metadata but are not saved in the database, making them ideal for computed or transient values.

**Sources**
- [SAP Capire - Virtual Elements](https://cap.cloud.sap/docs/cds/cdl#virtual-elements)