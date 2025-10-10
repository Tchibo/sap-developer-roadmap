---
tags:
  - localization
  - basic
links:
source:
aliases:
---
When developing [[Fiori Elements]] based user interfaces, it is possible to localise labels, tooltips and texts (such as for error messages) so that the user interfaces can also be used across languages.

To localise a field, the static label is replaced by an expression such as `{i18n>LABEL_NAME}`. The corresponding value for `LABEL_NAME` is maintained in the corresponding localisation file (usually `i18n_<COUNTRY_CODE>.properties`) of the target language. The user interface automatically displays the label or text in the correct language based on the user's language settings. With this approach, all texts to be displayed are managed centrally and can be translated or updated.

**Sources**
- [SAP Capire - Cookbook Localization](https://cap.cloud.sap/docs/guides/i18n)
- [SAP Capire  - Localization/i18n](https://cap.cloud.sap/docs/node.js/cds-i18n)
- [SAP UI5 Demo Kit - Localization of UI Texts](https://sapui5.hana.ondemand.com/#/topic/b8cb649973534f08a6047692f8c6830d)