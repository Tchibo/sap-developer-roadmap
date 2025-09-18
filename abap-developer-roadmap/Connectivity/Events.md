#basic
Event Driven Architecture (EDA) is an integration paradigm, that allows systems to communicate asynchronously and decoupled in near real time. Here an event producer publishes events, while a subscriber can consume the events whenever it suits them.

The event is in this context the payload with the information and it contains the change of a business object. 
We differ between two types of events:
- notification events typically carry only the identifier of the changed business object. Its purpose is to signal that something happened. 
- data events typically contains all necessary information for the consumer to act. Its purpose is to communicate what happened and to transfer the state of a certain object from publisher to subscriber. 

Event carried state transfer basically means that the event is the vehicle that carries the data representing the new state from the publisher to the subscriber system(s). This only applies to the data events since with notification events the subscriber always have to request the current state of the object. 

Notification Events risk creating an API bottleneck and decrease system decoupling, but compared to data events, they reduce payload sizes and the risk of out-of-order event processing. SAP only provides notification events so that the use of data events requires additional effort. (f.e. via RAP extensions).

Events in SAP use the Cloud Events standard as the standardized message format. The specification for the asynchronous APIs that handle these events is described using Async API.
### Resources
#website[A Beginner's Guide to Event-Driven Architecture](https://www.kurrent.io/event-driven-architecture)
#website [What Is Event-Driven Architecture?](https://docs.solace.com/Get-Started/event-mesh-basics.htm)
#website[Advanced Event Mesh Tutorials](https://help.pubsub.em.services.cloud.sap/Cloud/ggs_signup.htm)
#website [Enhance SAP with Advanced Event Mesh | Solace](https://solace.com/blog/enhance-sap-with-advanced-event-mesh/)
