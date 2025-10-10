---
tags:
  - test
  - advanced
  - do-not-publish
links:
  - "[[Testing]]"
source:
aliases:
  - end-to-end tests
---
> [!WARNING] Disclaimer
> At the time of writing, I have not yet gained hands-on experience with automated end-to-end (E2E) testing in [[SAP Capire]] projects.

End-to-end (E2E) testing verifies the complete flow of an application from the user's perspective, ensuring that all components—frontend, backend, database, and external interfaces—work together as expected in a production-like environment. Unlike unit or integration tests, E2E tests simulate real user scenarios.

A common approach is using the [[BDD]] framework **[[Cucumber]]**, which allows you to define test scenarios in human-readable `.feature` files using [[Gherkin]] syntax. Each step is mapped to a step definition in [[JavaScript]], which interacts with the application.

For [[SAP Capire]] projects, E2E testing with [[Cucumber]] is supported by the community plugin [`@cap-js-community/cds-cucumber`](https://www.npmjs.com/package/@cap-js-community/cds-cucumber). This plugin allows defining [[Gherkin]]-based test scenarios that interact with [[SAP Capire]] services. However, E2E testing still requires significant effort, including launching the full application stack and preparing test data.

E2E testing is most useful for critical user journeys where failures would cause high business risk, such as checkout flows or integration with external services. Due to their complexity, E2E tests should be applied selectively.

**Summary**  
E2E testing simulates complete user workflows to ensure all application components function correctly. In [[SAP Capire]] projects, the `@cap-js-community/cds-cucumber` plugin enables structured E2E testing with [[Gherkin]]. While the plugin helps, E2E testing requires significant setup and should be used for critical business flows.

**Sources**
- [Cucumber - Website](https://cucumber.io/)
- [CDS for Cucumber - Docmentation](https://cap-js-community.github.io/cds-cucumber/)
- [GitHub - @cap-js-community/cds-cucumber](https://github.com/cap-js-community/cds-cucumber)