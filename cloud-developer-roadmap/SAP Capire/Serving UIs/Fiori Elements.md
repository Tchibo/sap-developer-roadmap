---
tags:
  - frontend
  - fiori-elements
  - basic
links:
source:
aliases:
  - SAP Fiori Elements
---
SAP Fiori Elements is a framework that provides pre-defined floorplans for UI design, such as [[List Report]] and [[Object Page]]. It enables [[SAP UI5]] applications driven by [[OData]] services to be rendered automatically based on metadata and annotations, rather than custom UI logic. Developers annotate their [[CDS]] service definitions to define UI behavior and layout without writing [[JavaScript]] controllers for most scenarios.

Fiori Elements uses an annotation-based model for automated UI rendering. Annotations define UI elements like selection fields, line items, and navigation, ensuring the UI renders consistently with [[SAP Fiori design guidelines]]. It handles features like message handling, edit flow, and draft support out of the box, speeding up development.


> [!todo] Fiori Tools do not generate a Fiori app
> Fiori Tools merely assist in configuring the floorplan for a specific use case. Rendering in the browser occurs based on annotations in the browser. No pre-compiled content is deployed to the HTML5 repo.


> [!NOTE]
> [[SAP Capire]] fully supports Fiori Elements as its standard UI layer. Developers can annotate service entities with `@odata.draft.enabled` and UI annotations like `@UI.LineItem` in `.cds` files. [[SAP Fiori Tools]] can then generate the Fiori Elements front-end automatically.

**Summary**
SAP Fiori Elements is an annotation-driven UI framework that accelerates [[SAPUI5]] application development by generating consistent UIs from [[CDS]] models. It provides ready-to-use floorplans and handles complex UI behavior automatically.

**Sources**
- [GitHub - `@SAP-samples/fiori-elements-feature-showcase`](https://github.com/SAP-samples/fiori-elements-feature-showcase)
- [SAP Capire - Common Annotations](https://cap.cloud.sap/docs/cds/annotations)
- [SAPUI5 Demo Kit](https://sapui5.hana.ondemand.com/)