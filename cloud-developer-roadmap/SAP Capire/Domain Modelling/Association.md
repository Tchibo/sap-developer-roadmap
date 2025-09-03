---
tags:
  - cap-cds
  - cds
  - cdl
  - basic
links:
  - "[[Composition]]"
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/guides/domain-modeling#associations
aliases:
  - association
  - associations
---
With the help of an `association` (as with a [[Composition]]) relations can be formed between two entities.

> ==**Tip**==
> ==Differences between [[association vs. composition]]==

**unmanaged**
An "unmanaged association" is linked to the target entity using an existing foreign key and an `ON` condition which links our existing foreign key to the target entity.

**manged**
With an "managed association", a foreign key is not explicitly created (by the developer himself), but is created and managed by the [[CDL]] itself.

**Sources**
- [SAP Capire - CDL Association](https://cap.cloud.sap/docs/cds/cdl#associations)
- [SAP Capire - Data Modelling Associations](https://cap.cloud.sap/docs/guides/domain-modeling#associations)