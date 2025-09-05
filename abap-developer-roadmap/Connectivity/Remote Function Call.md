- [ ] Only mention the binary format once.
	- [ ] hab ich umgeschrieben - Absatz über Usage
- [ ] How can I call RFC from non-SAP? Via an URL?
	- [ ] das Zauberwort heißt JCO - respektive einfach nicht RFC verwenden :-D - siehe Anmerkung

Remote Function Call (RFC) is a proprietary data protocol for the data exchange between SAP systems. The RFC mechanism serializes the parameters and structures of function modules into a binary protocol for transfer via network connections. The SAP RFC libraries (e.g. SAP NetWeaver RFC Library) serialize and deserialize this data automatically when it is sent or received. 

The implementation of RFC makes communication between SAP systems more efficient but also integration to Non SAP system more difficult. For integration from NonSAP to SAP a wrapper  like the Java Connector was used in the past, which translates f.e. a REST call in Java into a RFC call to SAP.
### Usage

*Synchronous RFC* are used for direct communication to other systems or functions, were an immediate answer is needed. The process waits until the response is provided. 

When using *Asynchronous RFC* the process doesn't wait for an answer of the requested system or function and continues. The response is given and processed asynchronous making this kind also very widely used for parallelization purposes within SAP.

With Background RFC (bgRFC) the process places an asynchronous request into a queue that is processed in background. The bgRFC framework provides optimized processing, load distribution and error monitoring.

There also existing some older variants like transactional RFC and queued RFC that are deprecated and should be used any longer.

SAP also offers BAPI RFCs that encapsulate complete business objects as APIs, whereby these are increasingly being replaced by Business Object Interfaces (see also [Business Object Interfaces | SAP S/4HANA Cloud Private Edition | SAP Business Accelerator Hub](https://api.sap.com/products/SAPS4HANACloudPrivateEdition/onstackextensibility/bointerface)). 

The Java connector shouldn't be used any longer for integration purposes from NonSAP to SAP. Instead REST Based access like oData should be prefered.
### Ressources
#website RFC types and setup in SAP Help Portal [RFC | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/753088fc00704d0a80e7fbd6803c8adb/4888068ad9134076e10000000a42189d.html?locale=en-US)
[Background Communication | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/753088fc00704d0a80e7fbd6803c8adb/4896e29a0eec3987e10000000a421937.html?locale=en-US)
