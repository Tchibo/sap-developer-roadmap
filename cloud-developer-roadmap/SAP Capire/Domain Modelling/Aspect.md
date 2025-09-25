---
tags:
  - cap-cds
  - cds
  - cdl
  - basic
links:
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/cds/common#common-reuse-aspects
aliases:
  - aspect
  - aspects
  - Aspects
---
In the [[SAP Capire|CAP]] framework, an **aspect** is a reusable set of attributes that can be applied to multiple entities in different contexts. Aspects allow you to define common patterns, such as key definitions, amounts, or descriptive fields, once and reuse them across your data model. This improves consistency, reduces duplication, and makes maintenance easier. SAP provides frequently used aspects under the `sap.common` namespace, which can be implemented in custom entities.

**Example
```cds
aspect ContactInfo {
  email: String(100);
  phone: String(20);
}

// Apply aspect to a new entity
entity Customer : ContactInfo {
  key id : UUID;
  name    : String(100);
}

// Extend an existing entity with an aspect
entity Supplier {
  key id   : UUID;
  name     : String(100);
}

extend Supplier with ContactInfo;

```

In this example, both `Customer` and `Supplier` gain the `email` and `phone` attributes from the `ContactInfo` aspect without redefining them, illustrating how aspects help map common structures across entities. Aspects are especially useful when extending entities from external models or CDS plugins.

> [!TIP]
> The extension of entities is particularly helpful/useful if existing aspects or entities from a "foreign" data model or from a [[CDS plugin]] must/should be extended.

**Sources**
- https://cap.cloud.sap/docs/cds/common#common-reuse-aspects
- https://cap.cloud.sap/docs/cds/aspects
- [SAP Capire - Entites & Type Definitions](https://cap.cloud.sap/docs/cds/csn#type-definitions)