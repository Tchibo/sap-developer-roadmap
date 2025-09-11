
Was ist das Ziel des Artikels?
Technolie nicht Framework
Standard Events vs. Custom Events 
Verteilmöglichkeiten gen ED im Allgemeinen
Cloud Events & Async API


> [!NOTE] Vorschlag
> Erstmal definieren, was EDA ist bzw. was Events tun? Ist das hier zu viel?
> 
> Event Driven Architecture (EDA) is an integration paradigm, that allows systems to communicate asynchronously in near real time. An event producer creates (publishes) an event. Multiple systems can subscribe to this event and process it when they are ready to do so. 

A business object event is a creation or change to a business object within SAP. 

>[!open]+ OPEN
> ist das so?
> 	- A business object event is triggered when a business object is created, changed or deleted.
> 	- -> Wird nicht automatisch erzeugt. Muss man schon im Code aufrufen.

- [ ] Das Notification event enthält ja gerade nicht die Information, was geändert wurde.😢Soweit ich weiß. Enthalten die nur die ID des Objektes. Vllt. können wir diesen Satz weglassen. Die Events werden ja im nächsten Absatz noch erklärt.
- [ ] event wird gewrofen wenn implementiert

This trigger causes a notification event, which contains the data about the change and the business object.

In general we can differ between **notification events** (very lean scope) and **data events** (large scope). SAP itself only produces notification events in the standard, so that afterwards a read of the object via pull is necessary. 

Alternatively it makes more sense to formulate a data event for the change yourself via a RAP extension of the business object in order to avoid the pull.
### Resources
#website[A Beginner's Guide to Event-Driven Architecture](https://www.kurrent.io/event-driven-architecture)
#website[Advanced Event Mesh Tutorials](https://help.pubsub.em.services.cloud.sap/Cloud/ggs_signup.htm)
#website [Enhance SAP with Advanced Event Mesh | Solace](https://solace.com/blog/enhance-sap-with-advanced-event-mesh/)