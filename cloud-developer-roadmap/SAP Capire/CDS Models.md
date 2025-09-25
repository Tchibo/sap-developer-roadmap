---
tags:
  - nodejs
  - basic
links:
  - "[[CAP NodeJS Backend]]"
  - "[[JavaScript]]"
  - "[[Domain Entites]]"
  - "[[Domain Modelling]]"
  - "[[Service Definition]]"
  - "[[TypeScript]]"
source:
aliases:
  - "#cds-models"
  - "@cds-models"
---

> [!todo] The title 'cds-models' gives the impression of an executable command
> Should it not be called called 'CDS models' rather? Even though you refer to cds-typer documentation it would help here that 'cds --add typer' invokes the TypeScript model generation in the CAP project.

[[CDS]]-models in the [[SAP Capire]] Framework are type definitions for [[CDS]] entities, typically located in the `db` and `srv` folders. These types can be generated using [[cds-typer]] to enable type-safe development in [[TypeScript]].

By generating type definitions from [[CDS]] models, developers ensure their [[TypeScript]] code uses accurate, up-to-date types, which reduces runtime errors and improves code quality. These types can also be used in [[JavaScript]] as enriched [[JS-Doc]] comments for better type safety. Automatic generation ensures that any changes to the data model are immediately reflected in the codebase after regeneration.

**Summary**  
[[CDS]]-models in [[SAP Capire]] are automatically generated type definitions for [[CDS]] entities, enabling type-safe development in [[TypeScript]] and improved type support in [[JavaScript]]. They are kept in sync with the data model using tools like [[cds-typer]].

**Sources**
- [SAP Capire - CDS Typer](https://cap.cloud.sap/docs/tools/cds-typer)
- [SAP Capire - TypeScript - Generating Model Types Automatically](https://cap.cloud.sap/docs/node.js/typescript#generating-model-types-automatically)