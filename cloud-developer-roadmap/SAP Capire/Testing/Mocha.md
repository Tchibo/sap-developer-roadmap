---
tags:
  - test
  - unit-test
  - integration-test
  - tool
  - intermediate
  - do-not-publish
links:
  - "[[Testing]]"
  - "[[Unit Tests]]"
source:
aliases:
---

Mocha is a flexible [[JavaScript]] test framework for [[Node.js]], supporting behaviour driven development (BDD) and test driven development (TDD). It provides functions like `describe` and `it` for structuring tests and allows using external assertion libraries like [[Chai]].

For [[SAP Capire]] projects, Mocha integrates with the `@cap-js/cds-test` library. The `cds.test()` function starts a [[SAP Capire|CAP]] server within a test suite, offering utilities like `GET`, `POST`, and service access. Tests should be in a `test/` directory and use `describe` blocks for proper server management.

The official [[SAP Capire]] documentation lists Mocha as a supported test runner alongside [[Jest]], recommending [[Chai]] for assertions. It's crucial to initialize `cds.test()` before accessing `cds` services to prevent environment issues.

Mocha offers a solid foundation for testing [[SAP Capire]] projects, especially for those who prefer a modular setup.

**Summary**
Mocha is a flexible test runner for Node.js. In [[SAP Capire]] projects, it pairs with the `cds.test` library for isolated service and API testing. The CAP documentation guides its use with Chai and `cds.test`.