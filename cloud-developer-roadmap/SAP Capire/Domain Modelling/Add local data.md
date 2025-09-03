---
tags:
  - mock-data
  - basic
links:
  - "[[Domain Modelling]]"
  - "[[Add local test data]]"
source: https://cap.cloud.sap/docs/guides/databases?impl-variant=node#providing-initial-data
aliases:
---
To add local data (available in the [[development environment]]) that can be used for testing the application or as initial data during [[Deployment|deployment]], csv files can be created that provide the data during [[Deployment|development]].

It is also recommended to save data that is to be provided initially (e.g. for [[Value-Helps]]) in local csv files as these are automatically transferred to the target [[database]] during [[Deployment]] and are directly available.

>[!TIP]
The command `cds add data` (from the [[cds CLI]]) can be used to create empty [[CSV]] files (under `db/data`) for all defined entities, which then only need to be filled with the required information.

**Sources
- [SAP Capire - Provide initial data](https://cap.cloud.sap/docs/guides/databases?impl-variant=node#providing-initial-data)
