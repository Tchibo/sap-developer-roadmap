---
tags:
  - cds
  - cdl
  - basic
links:
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/cds/cdl#entities-type-definitions
aliases:
---
Type definitions in [[SAP Capire]] allow developers to define reusable, named data types that ensure consistency across multiple entities and elements in a [[Domain Modelling|domain model]]. By abstracting commonly used structures or value types, type definitions simplify maintenance and promote clarity in the model. Type definitions can be used for simple value types, such as strings or numbers with specific formats, as well as for enumerations that restrict values to a predefined set.

> [!TIP]
A type definition can be referenced in multiple entities or elements, making it easier to apply consistent validation rules and formatting throughout the domain model.

**Example**
```cds
type PhoneNumber : String(20);
type Status : String enum { Active; Inactive; };
entity Customer {
  key ID         : UUID;
      name       : String;
      phone      : PhoneNumber;
      status     : Status;
}
```

**Summary**  
Type definitions in [[SAP Capire]] enable the creation of reusable and consistent data types that can be referenced throughout domain models. This helps maintain consistency, improve readability, and reduce duplication in entity definitions.

**Sources**
- [SAP Capire - Entites & Type Definitions](https://cap.cloud.sap/docs/cds/csn#type-definitions)
- [SAP Capire - CSN Type Definitions](https://cap.cloud.sap/docs/cds/csn#type-definitions)
- [SAP Capire - Typer Enums](https://cap.cloud.sap/docs/cds/csn#type-definitions)