#intermediate 
The SAP Web Dispatcher is not part of ABAP Platform. Technically it is located between the Internet and your SAP system. 

It is the entry point for HTTP(s) requests into your system and as a “software web switch”, SAP Web Dispatcher can reject or accept connections. When it accepts a connection, it balances the load to ensure an even distribution across the servers. 

SAP Web Dispatcher therefore contributes to security and also balances the load in your SAP system.

The SAP Web Dispatcher is only useful when interacting with web applications or http requests. It forwards incoming requests to the application servers and returns the responses from the backend to the client. Outgoing requests (such as requests to another Application Server) are not sent using the SAP Web Dispatcher. 

 In the classic SAP system with its RFC handling, load is balanced by the message server - for example in the use case of parallelization.

While ICM and SAP Web Dispatcher share the same code base, they account for different tasks.
The SAP Web Dispatcher performs load balancing, and passes requests forward to ICMs on the application servers.
### Resources
#website [Collective SAP Note Web Dispatcher 538405](https://help.sap.com/docs/link-disclaimer?site=https://me.sap.com/notes/538405)
#website [Architecture and Functions of the SAP Web Dispatcher | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/683d6a1797a34730a6e005d1e8de6f22/4899ac3a7f020e27e10000000a421937.html?locale=en-US)