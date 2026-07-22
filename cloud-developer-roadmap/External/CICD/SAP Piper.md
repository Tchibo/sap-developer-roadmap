---
tags:
  - sap-cloud-developer-roadmap
  - ci/cd
  - tool
links:
source:
aliases:
  - SAP Project Piper
  - Project Piper
AI generated: true
---
SAP Project Piper is an open source framework provided by SAP that delivers reusable pipeline components for implementing continuous integration and continuous delivery in SAP centric development scenarios. It serves as the technical foundation for standardized pipeline execution by offering a collection of predefined steps, stages, and best practices that can be integrated into [[CICD|CI/CD]] systems such as [[Jenkins]] or the [[SAP Continuous Integration and Delivery|SAP CI/CD]] service.

The framework is implemented primarily in [[Groovy]] and [[YAML]] and is designed to be used within [[Jenkins]] based environments. It provides a shared library that encapsulates common pipeline logic, enabling developers to define pipelines in a simplified and consistent way. Instead of building pipelines from scratch, teams can leverage Piper steps that handle tasks such as building applications, running tests, and deploying artifacts to SAP environments. This approach reduces complexity and ensures alignment with SAP recommended development processes.

A key aspect of SAP Project Piper is its extensibility and strong integration with SAP technologies. It supports scenarios such as [[SAP Capire|SAP Cloud Application Programming Model]] development and integrates with services like transport management and cloud deployment targets. By abstracting complex pipeline logic into reusable components, SAP Project Piper enables scalable and maintainable automation while enforcing best practices across development teams.

**Summary**
SAP Project Piper is an open source framework that provides reusable pipeline components and standardized logic for [[CICD|CI/CD]] in SAP environments, enabling consistent and scalable automation based on SAP best practices.

**Sources**
- [Documentation - Project Piper](https://www.project-piper.io/)
- [GitHub - Project Piper Action](https://github.com/SAP/project-piper-action)
- [GitHub - jenkins-library](https://github.com/SAP/jenkins-library)