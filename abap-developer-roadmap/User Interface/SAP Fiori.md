#basic 

**SAP Fiori** applications use the **SAPUI5** JavaScript client library to render user interfaces as 'Single Page Applications' in the web browser. SAPUI5 based applications that respect the Fiori Design Guidelines are called SAP Fiori applications.

SAPUI5 is a stateless, client side UI technology for rendering in web browsers. 'Stateless' refers to the fact that the ABAP application server does not keep track of the state of a user session between user interactions, 'client side' refers to the fact that UI components are processed in the web browser on the client device to render the UI. Backend requests from a SAPUI5 application to the ABAP Platform transport only the data that needs to be rendered. The UI's html content is created in the browser based on SAPUI5 JavaScript logic and merged with the data received in REST calls from the ABAP backend. 

**Fiori Elements** describes the approach of using SAP Fiori template apps that are configured for UI rendering of custom built data models. Using configured Fiori Elements template apps removes the need to code UI behaviour and caters for metadata driven UI rendering based on data model annotations stemming from the ABAP backend. Fiori Elements template apps are available in various floorplans for different use cases.

## Further reading
#article [Single Page Application](https://en.wikipedia.org/wiki/Single-page_application)
#article [Fiori Design Guidelines](https://www.sap.com/design-system/fiori-design-web/?external)
#article [SAPUI5 development kit](ui5.sap.com)
