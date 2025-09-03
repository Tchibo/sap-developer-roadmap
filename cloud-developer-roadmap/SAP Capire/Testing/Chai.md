---
tags:
  - test
  - unit-test
  - tool
  - integration-test
  - intermediate
links:
source:
aliases:
---
>Chai is a BDD / TDD assertion library for [node](http://nodejs.org/) and the browser that can be delightfully paired with any [[JavaScript]] testing framework.
>*~https://www.chaijs.com/*

Chai is a popular assertion library for [[JavaScript]] used with test frameworks like [[Mocha]] and [[Jest]], and is also supported by [[cds-test]]. It provides an expressive syntax for writing assertions, with styles like `expect`, `should`, and `assert`.

In [[SAP Capire]] projects with [[Node.js]], Chai is recommended for use with the `@cap-js/cds-test` library. The `cds.test()` utility integrates Chai out-of-the-box and provides shortcuts for writing assertions, ensuring test portability across different runners.

> [!WARNING]
> Using `chai` requires adding these dependencies to your project:
> ```
npm add -D chai@4 chai-as-promised@7 chai-subset jest

These plugins enable features like assertions on promises (`chai-as-promised`) and partial object matching (`chai-subset`). For more details, see the [[SAP Capire]] test documentation for Chai.

**Summary**
Chai is a flexible assertion library for [[JavaScript]] that improves the readability of test validations. In [[SAP Capire]] projects, it integrates with `cds.test()` and can be added via `npm`.

**Sources**
- [Chai - Website](https://www.chaijs.com/)
- [SAP Capire - Testing with `cds.test`](https://cap.cloud.sap/docs/node.js/cds-test)
- [SAP Capire - `cds.test.Test.chai`](https://cap.cloud.sap/docs/node.js/cds-test#chai)