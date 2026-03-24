---
tags:
  - sap-cloud-developer-roadmap
  - ci/cd
  - service
  - runtime
links:
source:
aliases:
  - SAP CI/CD
AI generated: true
---
The SAP Continuous Integration and Delivery service is a managed service provided by SAP on the [[SAP BTP|SAP Business Technology Platform]] that enables automated continuous integration and continuous delivery pipelines for cloud based applications. Its technical foundation is based on the open source project [[SAP Piper|Project Piper]], which provides reusable pipeline logic and predefined steps tailored for SAP development scenarios. The service internally leverages container based execution and [[Kubernetes]] orchestration to ensure scalable and isolated pipeline runs.

Pipelines are defined as code using [[YAML]] configuration files and are executed through a [[Jenkins]] based runtime that is abstracted from the user. This allows developers to focus on pipeline configuration without managing the underlying infrastructure. The service integrates with [[Git]] repositories and uses predefined stages such as build, test, and deploy, which are implemented through modular pipeline steps provided by [[SAP Piper|Project Piper]]. These steps encapsulate SAP specific best practices and standardize interactions with services such as transport management and deployment targets.

A key advantage of the SAP CI/CD service is its deep integration into the SAP ecosystem combined with its standardized technical architecture. By combining [[Jenkins]], [[Kubernetes]], and [[SAP Piper|Project Piper]], the service provides a robust and extensible foundation for enterprise grade automation while ensuring consistency, security, and compliance with SAP development guidelines.

**Summary**
The SAP Continuous Integration and Delivery service is built on [[SAP Piper|Project Piper]], [[Jenkins]], and [[Kubernetes]], providing container based and scalable pipeline execution with predefined SAP specific steps, while abstracting infrastructure complexity for developers.

**Sources**
- [SAP Discovery Center - SAP CI/CD Service](https://discovery-center.cloud.sap/serviceCatalog/continuous-integration--delivery)
- [SAP Help - SAP Continuous Integration and Delivery](https://help.sap.com/docs/CONTINUOUS_DELIVERY)
- [Tchibo Confluence - Exploration of SAP CI/CD Service](https://tchibo.atlassian.net/wiki/x/IACnEQ)