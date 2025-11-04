---
tags:
  - cap-cds
  - intermediate
links:
  - "[[Domain Entites]]"
  - "[[Views & Projections]]"
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/cds/cdl#calculated-elements
aliases:
---
In [[SAP Capire]], entities and aspects support _calculated elements_, allowing the specification of value expressions or expressions that resolve to [[Association|associations]]. These elements are **read-only** and automatically computed, meaning no manual input is needed during write operations.

There are two main types:
- **On-read calculated elements**: Evaluated when the data is read. They act like expression macros and are replaced in queries with their defining expressions. These improve reusability and avoid redundant code. However, they come with restrictions: no subqueries, no nested projections, and they can’t be keys or used in certain association conditions.
- **On-write calculated elements** (defined with `stored`): Evaluated during write operations and persisted to the database, improving performance in queries (e.g., for sorting/filtering). They must only refer to elements within the same row and cannot include subqueries or paths with associations.

Additionally, _association-like calculated elements_ use filtered [[associations]] with inline filters and are useful for exposing pre-filtered relations without defining a separate view.

**Summary**  
[[SAP Capire|CAP]] supports calculated elements in [[CDS]] models for improved code clarity and performance. On-read elements are dynamically evaluated at read time, while on-write elements are precomputed and stored. Filtered associations can also be expressed as calculated elements. Each type comes with specific restrictions and benefits.

**Sources**
- [SAP Capire - Calculated Elements](https://cap.cloud.sap/docs/cds/cdl#calculated-elements)