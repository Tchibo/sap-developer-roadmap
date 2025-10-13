---
tags:
  - fiori-elements
  - basic
links:
source:
aliases:
  - Draft
  - drafts
  - draft
---
In [[SAP Capire]], Draft Handling allows users to work on data in an intermediate state before final saving. This is useful for complex transactional data entry that requires intermediate saves and validations. Drafts are implemented using the `@odata.draft.enabled` annotation, which makes [[SAP Capire]] automatically generate the necessary infrastructure, including a shadow draft table and actions like `EDIT`, `ACTIVATE`, and `CANCEL`.

[[SAP Capire]] uses [[OData v4]] to manage draft lifecycles, distinguishing between *active* and *draft* entities. When a user edits an active entity, a draft version is created, which can be saved or discarded. Once finalized, the draft is "activated," replacing or creating the active version.

Key features include:
- **Optimistic Locking:** Prevents conflicting edits.
- **Automatic Draft Cleanup:** Deletes old drafts.
- **Custom Validation:** Allows developers to add custom logic.

Draft support in [[SAP Capire]] simplifies transactional consistency and collaboration, letting developers focus on business logic.

**Summary**
Draft Handling in [[SAP Capire]] enables users to manage intermediate data versions before committing changes. It's integrated with [[OData v4]] and supports features like lifecycle actions, optimistic locking, and custom validations.

**Sources**
- [SAP Capire - Draft Support](https://cap.cloud.sap/docs/advanced/fiori#draft-support)
- [SAP Capire - Lean Draft](https://cap.cloud.sap/docs/node.js/fiori#lean-draft)