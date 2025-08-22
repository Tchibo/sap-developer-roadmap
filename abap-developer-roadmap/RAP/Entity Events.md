#Advanced

A RAP business object can raise entity events to signal state changes (for example, “Order created” or “Product briefing finished”). Events are declared in the behavior definition and are raised in the behavior implementation with `RAISE ENTITY EVENT` after the changes are committed (in the additional save sequence).

Events can be consumed **locally** or **remotely**. Local consumption uses ABAP Objects event handler classes. Remote consumption uses ABAP Push Channels (APC) to deliver events over WebSocket directly to consumers or via a broker such as SAP Event Mesh or SAP Advanced Event Mesh.

SAP standard business objects typically raise business events that carry only the key fields of the affected instance (notification events). A data event includes all fields of a business object. Standard notification events can be remodeled as data events using a behavior extension.
## Resources
- #website [Business Events | SAP Help Portal](https://help.sap.com/docs/abap-cloud/abap-rap/business-events?locale=en-US)
- #website [Raise Business Event | SAP Help Portal](https://help.sap.com/docs/abap-cloud/abap-rap/concept-business-events?locale=en-US)
- #website  [Business Event Consumption](https://help.sap.com/docs/abap-cloud/abap-rap/business-event-consumption?locale=en-US)
- #article [How to Create RAP Business Events in SAP BTP ABAP ... - SAP Community](https://community.sap.com/t5/technology-blog-posts-by-sap/how-to-create-rap-business-events-in-sap-btp-abap-environment/ba-p/13546199)