---
tags:
  - events
  - event-driven-architecture
  - advanced
links:
  - "[[Add external services]]"
  - "[[Business Accelerator Hub]]"
  - "[[Event Driven Architecture]]"
source:
aliases:
---
> [!quote] [*SAP Capire Documentation*](https://cap.cloud.sap/docs/guides/messaging/#events-and-messaging)
> CAP provides intrinsic support for emitting and receiving events. This is complemented by Messaging Services connecting to message brokers to exchange event messages across remote services.

> [!todo] Provide more input about the how-to in CAP
> Make reference to the 'cds --add enterprise-messaging --cloudevents' statement and indicate what that will do to the node.js CAP project.

[[SAP Capire]] provides strong support for event-driven development by enabling applications to publish and consume events in a standardized way. Through its built-in APIs and integration with messaging services, [[SAP Capire|CAP]] applications can easily interact with external systems and cloud environments using events. This architecture helps decouple services and allows for scalable solutions where communication happens through events rather than direct dependencies.

[[SAP Capire]] supports integration with messaging services, making it possible for applications to connect with message brokers and exchange events across different systems. The supported brokers currently include [[SAP Event Mesh]], [[SAP Advanced Event Mesh]], [[SAP Event Broker]], and [[Redis PubSub]]. This capability helps ensure that [[SAP Capire|Capire]] applications can be extended and integrated within larger [[Event Driven Architecture|event-driven architectures]].

**Summary**
[[SAP Capire]] natively supports event-driven development by providing APIs and abstractions for publishing and handling events, and by integrating with messaging services to connect with external brokers. Supported brokers include [[SAP Event Mesh]], [[SAP Advanced Event Mesh]], [[SAP Event Broker]], [[Redis PubSub]]. (There might be more supported brokers in the future)

**Sources**
- [SAP Capire - Events and Messaging](https://cap.cloud.sap/docs/guides/messaging/)
- [SAP Capire - `cds.Event`](https://cap.cloud.sap/docs/node.js/events#cds-event)
- [SAP Capire - `cds.MessagingService`](https://cap.cloud.sap/docs/node.js/messaging#cds-messagingservice-class)