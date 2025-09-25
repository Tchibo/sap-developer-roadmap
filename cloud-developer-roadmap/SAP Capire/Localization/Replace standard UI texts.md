---
tags:
  - localization
  - rework
  - advanced
links:
source:
aliases:
---
Standard texts in a [[Fiori Elements]] user interface can be customised either globally for the entire application or specifically for certain entities or actions. This allows, for example, displaying a custom message when confirming a business partner. To achieve this, a localisation file is created and referenced in the application's `manifest.json`, overriding the default texts.

To replace standard UI texts, create a `customI18N.properties` file (the name can vary) and reference it in the manifest:

```json
"RootEntityListReport": {
    ...
    "options": {
        "settings": {
            ...
            "enhanceI18n": "i18n/customI18N.properties",
            ...
        }
    }
},
```

Customisations can target all entities, specific entities, or specific actions of entities. Examples of keys include:
- `C_COMMON_DIALOG_OK` for all entities
- `C_TRANSACTION_HELPER_OBJECT_PAGE_CONFIRM_DELETE_WITH_OBJECTTITLE_SINGULAR|RootEntities` for the "RootEntities" entity
- `C_OPERATIONS_ACTION_CONFIRM_MESSAGE|RootEntities|criticalAction` for the "criticalAction" action of the "RootEntities" entity
- `C_COMMON_ACTION_PARAMETER_DIALOG_CANCEL|RootEntities` for a custom cancel text

**Sources**
- [GitHub SAP Samples/fiori-elements-feature-showcase - Replacing standard UI texts](https://github.com/SAP-samples/fiori-elements-feature-showcase?tab=readme-ov-file#replacing-standard-ui-texts)