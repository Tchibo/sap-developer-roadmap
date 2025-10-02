---
tags:
  - cap-cds
  - cds
  - cdl
  - basic
links:
  - "[[Association]]"
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/guides/domain-modeling#compositions
aliases:
  - composition
---
  A `composition` in [[SAP Capire|CAP]] is a special kind of association that establishes a strong parent-child relationship between entities, where the child entity’s lifecycle is strictly dependent on the parent. If the parent entity is deleted, all composed children are deleted as well. This makes composition suitable for modeling scenarios where a child cannot exist independently of its parent, such as items within an order or addresses within a customer.

In [[CDS]], a composition is declared using the `composition of` keyword. This is primarily used to model contained-in or whole-part relationships within domain models.

**Example**
```cds
entity Order {
  key ID     : UUID;
      items  : Composition of many OrderItem on items.parent = $self;
}

entity OrderItem {
  key ID     : UUID;
      parent : Association to Order;
      product: String;
      amount : Integer;
}
```

**Summary**  
A composition defines a contained-in relationship between entities where the child entity’s lifecycle is tied to the parent, making it ideal for parent-to-child models. If the parent is removed, the children are also deleted.

**Sources**
- [SAP Capire - CDS Compositions](https://cap.cloud.sap/docs/cds/cdl#compositions)
- [SAP Capire - Domain Modelling Compositions](https://cap.cloud.sap/docs/guides/domain-modeling#compositions)