The ICM is a component of Application Server ABAP. It is implemented as a separate process, which is started and monitored by the ABAP dispatcher.

The Internet Communication Manager ensures the communication between the SAP system and the outside world. In its role as server it processes requests from the Internet. The processing of URL requests is dependent on the configured server/port combination. Depending on the URL the ICM calls the relevant local handler.

You need the ICM if you want your AS ABAP to communicate with the Internet via HTTP, HTTPS or SMTP, like Web applications do with Web Dynpro ABAP.

While ICM and SAP Web Dispatcher share the same code base, they account for different tasks. The SAP Web Dispatcher performs load balancing, and passes requests to ICMs on the connected application servers which then passes it further to handler running on work processes. This relationship makes it possible to share profile parameters and administration options. 
### Resources
[Architecture of the Internet Communication Manager (ICM) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/bd78479f4da741a59f5e2a418bd37908/c1bf5719da544accb89f326c252213ab.html?locale=en-US)