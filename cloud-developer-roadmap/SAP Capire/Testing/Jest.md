---
tags:
  - test
  - unit-test
  - integration-test
  - tool
  - intermediate
links:
  - "[[Testing]]"
  - "[[Unit Tests]]"
source:
aliases:
---
Jest is a modern [[JavaScript]] testing framework (with [[TypeScript]] support) maintained by Meta, used for unit, integration, and end-to-end testing of [[Node.js]] applications. It offers an all-in-one solution with a test runner, mocking, and assertion libraries.

In [[SAP Capire]] projects with a [[Node.js]] backend, Jest can be used with the [[cds-test]] library, which provides utilities for testing [[SAP Capire]] applications. Using `cds.test()`, you can start a [[SAP Capire]] server instance within your test suite, perform [[HTTP]] and service-level requests, and access preconfigured tools like `GET`, `POST`, and `expect`. This allows for writing isolated tests for service APIs, database interactions, and custom logic.

> [!TIP]
> The [[SAP Capire]] documentation recommends using Jest with the [[Chai]] assertion library for portable tests. Tests should be structured with `describe`, `it`, or `test` blocks and launched via `cds.test()`, which manages the [[SAP Capire]] server instance. Avoid Jest helpers like `resetModules` and `useFakeTimers`, as they can conflict with the [[SAP Capire]] runtime.

For guidance on configuring and running tests with Jest, refer to the official [[SAP Capire]] documentation.

**Summary**
Jest is a versatile test framework for [[Node.js]] applications. In [[SAP Capire]] projects, it integrates with `cds.test` to test service APIs and logic.

**Sources**
- [Jest - Documentation](https://jest.io)
- [SAP Capire - Testing with `cds.test`](https://cap.cloud.sap/docs/node.js/cds-test)
- [SAP Capire - Using Jest or Mocha](https://cap.cloud.sap/docs/node.js/cds-test#using-jest-or-mocha)