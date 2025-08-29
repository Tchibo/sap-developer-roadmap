### Push Communication
**Push communication** is a point to point messaging pattern where the provider actively initiates and delivers information to the consumer without the recipient requesting it. One example for push communication is the distribution of assortment lists by IDoc.
### Pull Communication
**Pull communication** is a point to point messaging pattern where the consumer actively requests and retrieves information from the provider. One example is an OData request to the backend from a Fiori app.
### PubSub Communication
**Publish & Subscribe communication** is a decoupled messaging pattern where publishers send messages to topics without knowing who will receive them, while subscribers listen to specific topics and receive messages without knowing who sent them.
### Synchronous communication
**Synchronous communication** is a method where the sender transmits a message and waits for an immediate response from the receiver before continuing. One example is an OData request to the backend from a Fiori app.
### Asynchronous communication
**Asynchronous communication** is a method where the sender transmits a message and continues processing without waiting for an immediate response from the receiver. Examples for asynchronous messaging are PubSub in general but also IDoc messages.
### Process vs. Data Integration
**Process integration** focuses on integration of **business objects** between systems (mainly on Application server level), while **data integration** focuses on combining, transforming and moving of mass **data** between systems (mainly on database level).
### User Integration
**User integration** is the seamless connection of user interfaces and experiences across multiple systems without needing to switch between separate interfaces.
### Functional User vs. Principal Propagation
The **Functional user** is a technical service account used for system-to-system communication, while **principal propagation** passes the actual end-user's identity through the entire call chain so that backend systems know who the real user is.