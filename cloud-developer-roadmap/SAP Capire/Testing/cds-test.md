---
tags:
  - test
  - unit-test
  - tool
  - integration-test
  - intermediate
links:
  - "[[Testing]]"
  - "[[Unit Tests]]"
source:
aliases:
  - "@cap-js/cds-test"
---
The `@cap-js/cds-test` package is an official SAP library for testing [[SAP Capire]] projects with a [[Node.js]] backend. It provides utilities for testing service APIs, database behavior, and business logic.

This library simplifies the testing setup by allowing [[SAP Capire]] instances to be launched programmatically with `cds.test()`. This function manages the server context and lifecycle using hooks like `beforeAll` and `afterAll`. It also provides bound [[HTTP]] methods (`GET`, `POST`) and access to [[SAP Capire]] services via `cds.connect.to()`, enabling both [[HTTP]]-level and service-level testing. The library includes preconfigured [[Chai]] assertions and is compatible with test runners like [[Mocha]] and [[Jest]].

`@cap-js/cds-test` also introduces practices for reliable testing, such as automatic database reset with `test.data.reset()` and safe test initialization to avoid side effects.

> [!TIP]
> At Tchibo, we use `@cap-js/cds-test` for testing [[SAP Capire]] projects, often without separate test runners like [[Jest]] or [[Mocha]], to streamline our setup and align with SAP's official tooling.

**Summary**
`@cap-js/cds-test` is the official SAP library for testing [[SAP Capire]] [[Node.js]] projects. It offers tools for API and service testing, integrates with [[SAP Capire]] servers, and includes [[Chai]] support.

**Sources**
- [SAP Capire - Testing with `cds.test`](https://cap.cloud.sap/docs/node.js/cds-test#testing-with-cds-test)
- [GitHub - @cap-js/cds-test](https://github.com/cap-js/cds-test)