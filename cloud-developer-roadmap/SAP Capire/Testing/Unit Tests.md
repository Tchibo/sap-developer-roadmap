---
tags:
  - unit-test
  - test
  - intermediate
links:
  - "[[Testing]]"
source:
aliases:
---
Unit tests help ensure that our application produces both technically correct and business-compliant results. In a [[SAP Capire]] project based on [[Node.js]], writing such unit tests is supported primarily by the [`@cap-js/cds-test`](https://www.npmjs.com/package/@cap-js/cds-test) package developed and maintained by SAP.
This package is tailored for the [[SAP Capire|Capire]] framework  and provides essential utilities to test services, database operations, and even authentication/authorization flows (when running locally) effectively. It supports upon well-known JavaScript test frameworks like [[Jest]] and adds [[SAP Capire|Capire]]-specific capabilities such as:
- Initializing the [[SAP Capire|Capire]] service instance using `cds.test()`
- Easily mocking and loading data by defining thhem in csv files inside the `test/data` directory
- Support for [[SQLite]] in-memory as a lightweight test database
- Clearing/resetting the mocked data on demand

For [[SAP Capire]] projects, it is strongly recommended to use `@cap-js/cds-test` due to its deep integration with the [[SAP Capire|CAP]] framework and the fact that it is officially supported by SAP.

**Sources**
- [SAP Capire - Testing with `cds.test`](https://cap.cloud.sap/docs/node.js/cds-test)
- [SAP Community - Comprehensive Guide to Unit Testing in CAP](https://community.sap.com/t5/technology-blog-posts-by-sap/comprehensive-guide-to-unit-testing-in-cap/ba-p/13742918)