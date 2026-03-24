---
tags:
  - sap-cloud-developer-roadmap
  - ci/cd
  - runtime
links:
source: https://concourse-ci.org/
aliases:
AI generated: true
---
> Concourse is an open-source continuous thing-doer.

Concourse is an open source [[CICD|CI/CD]] system that focuses on automation, reproducibility, and scalability of software delivery pipelines. It is designed around the concept of pipelines that define how code is built, tested, and deployed. These pipelines are declarative and version controlled, which ensures that every change in the delivery process is transparent and traceable. Concourse uses resources to represent external dependencies such as [[Git]] repositories or container images, and jobs to define sequences of steps that act on these resources. This structure enables a clear separation between input, processing, and output within a pipeline.

A central characteristic of Concourse is its strong emphasis on immutability and container based execution. Every task runs in an isolated container, which guarantees consistent execution environments and eliminates issues caused by differences between development and production systems. This makes Concourse particularly suitable for cloud native development scenarios where reproducibility and reliability are critical.

The [[fly CLI]] is the primary command line interface used to interact with a Concourse deployment. It allows developers to log in to a Concourse instance, configure and update pipelines, trigger jobs, and monitor execution. The relationship between Concourse and [[fly CLI|fly]] is therefore essential, since Concourse provides the backend system that executes pipelines, while [[fly CLI|fly]] acts as the user interface for managing and controlling these processes. Without [[fly CLI|fly]], interacting with Concourse would be significantly more limited, as it encapsulates all operational commands required for day to day pipeline management.

**Summary**
Concourse is a [[CICD|CI/CD]] system that enables automated and reproducible pipelines using container based execution. The [[fly CLI]] is the command line tool that developers use to configure, trigger, and monitor these pipelines, making it the main interface for interacting with Concourse.

**Sources**
- [Concourse - Website](https://concourse-ci.org/)
- [Concourse - Documentation](https://concourse-ci.org/docs/)
- [Concourse - `fly` CLI Documentation](https://concourse-ci.org/docs/fly/)