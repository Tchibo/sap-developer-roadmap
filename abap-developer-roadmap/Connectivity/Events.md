A business object event is a creation or change to a business object within SAP. 

>[!open]+ OPEN
> ist das so?

This trigger causes a notification event, which contains the data about the change and the business object.

In general we can differ between notification events (very lean scope) and data events (large scope). SAP itself only produces notification events in the standard, so that afterwards a read of the object via pull is necessary. 
Alternatively it makes more sense to formulate a data event for the change yourself via a RAP extension of the business object in order to avoid the pull.
### Resources
#website[A Beginner's Guide to Event-Driven Architecture](https://www.kurrent.io/event-driven-architecture)
#website[Advanced Event Mesh Tutorials](https://help.pubsub.em.services.cloud.sap/Cloud/ggs_signup.htm)
#website [Enhance SAP with Advanced Event Mesh | Solace](https://solace.com/blog/enhance-sap-with-advanced-event-mesh/)