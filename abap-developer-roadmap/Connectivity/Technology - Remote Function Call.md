Remote Function Call (RFC) is a proprietary data protocol for the data exchange between SAP systems. The RFC mechanism serializes the parameters and structures of function modules into a binary protocol for transfer via network connections. The SAP RFC libraries (e.g. SAP NetWeaver RFC Library) serialize and deserialize this data automatically when it is sent or received. 

SAP RFC uses a binary format for data transfer by default, which makes communication efficient, but makes integration more difficult without SAP's own libraries.

### Usage

*Synchronous RFC* are used for direct communication to other systems or functions, were an immediate answer is needed. The process waits until the response is provided. 

When using *Asynchronous RFC* the process doesn't wait for an answer of the requested system or function and continues. The response is given and processed asynchronous making this kind also very widely used for parallization purposes within SAP.

With Background RFC (bgRFC) the process places an asynchronous request into a queue that is processed in background. The bgRFC framework provides optimized processing, load distribution and error monitoring.

There also existing some older variants like transactional RFC and queued RFC that are deprecated and should be used any longer.

SAP also offers BAPI RFCs that encapsulate complete business objects as APIs, whereby these are increasingly being replaced by Business Object Interfaces (see also [Business Object Interfaces | SAP S/4HANA Cloud Private Edition | SAP Business Accelerator Hub](https://api.sap.com/products/SAPS4HANACloudPrivateEdition/onstackextensibility/bointerface)). 


### Links
RFC types and setup in SAP Help Portal [RFC | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/753088fc00704d0a80e7fbd6803c8adb/4888068ad9134076e10000000a42189d.html?locale=en-US)
