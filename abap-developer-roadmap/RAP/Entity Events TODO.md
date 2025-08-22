#Advanced 
- [ ] #todo #edna read and adjust, if necessary

A RAP business object can raise entity events to signal state changes. In SAP standard, these events are typically fired on state transfer after the changes are committed to the database (post-commit).



A RAP business object has the ability to raise entity events to inform about a change in its state. In SAP Standard, entity events are typically raised on state transfer after the underlying changes to the BO data are irrevocably saved to the database. To ensure this,  using the `RAISE ENTITY EVENT` statement in the BO's behavior implementation.

Entity events that are raised in a provider system can be **remotely consumed** or **locally consumed**. Local consumption in the provider system is facilitated by global classes defined using ABAP Objects with the  'FOR EVENTS OF <BO>' statement. Consumption by remote consumer systems is facilitated by ABAP Push Channels that establish a websocket connection to the consumer or to a message broker like SAP (Advanced) Event Mesh. 

SAP Standard events are typically **notification events** (i.e. contain only the key of the BO that was affected by the event). Using a behaviour extension for a SAP Standard BO new BO event types can be defined to facilitate event driven state transfer using **data events**. The data event payload contains the latest attribute values of all entities in the BO composition. A consumer receiving the latest data event has an up to date view of the BO that changed its state in the provider system.

## Further reading

- #website  [Business Event Consumption](https://help.sap.com/docs/abap-cloud/abap-rap/business-event-consumption?locale=en-US)
- #website  [RAISE ENTITY EVENT | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABAPRAISE_ENTITY_EVENT.html)