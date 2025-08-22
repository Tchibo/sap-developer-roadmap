RFCs (Remote Function Call) can be used both to transfer data and to call up complete and complex functions in other systems.

A distinction is made between
- synchronous RFCs
- asynchronous RFCs
- transactional RFCs
- queued RFCs
- background RFC

SAP offers BAPI RFCs that encapsulate complete business objects as APIs, whereby these are increasingly being replaced by Business Object Interfaces (see also [Business Object Interfaces | SAP S/4HANA Cloud Private Edition | SAP Business Accelerator Hub](https://api.sap.com/products/SAPS4HANACloudPrivateEdition/onstackextensibility/bointerface)). 

### Usage
Of the five RFC types mentioned, only synchronous, asynchronous and background RFC should be used. They may only be used for communication between SAP onPrem systems.

### Links
RFC types and setup in SAP Help Portal [RFC | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/753088fc00704d0a80e7fbd6803c8adb/4888068ad9134076e10000000a42189d.html?locale=en-US)
