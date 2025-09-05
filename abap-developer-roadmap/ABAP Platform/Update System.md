In SAP a business process is mapped by means of a transaction, which can include several changes. The data changes caused by this process should be completely executed in the database, or not at all. (see also chapter logical unit of work / LUW)

This is ensured by the  SAP update system, which offers increased security, performance, and the ability to recover when making database changes.

For Updates you can basically differ between 
- V1 modules are processed consecutively in a single update work process on the same application server. These belong to a single database logical unit of work (LUW) and can be rolled back. V1 updates are executed under the SAP locks held by the transaction that generated the update. This ensures data consistency; concurrent changes to the objects to be updated are not possible.
- V2 updates are executed together in a separate LUW. They are not executed under the locks held by the transaction that generated them. If your SAP System contains a work process for V2 updates, these are only carried out in this work processes. Otherwise, the V2 components are processed by a V1 update process.
- V3: Beside V1 and V2 function modules, there are also “collective run” function modules. Unlike V1 and V2, these function modules are not updated automatically. They are only updated if report RSM13005 starts the update. Then, all the calls for the function module are collected, compressed (see example), and updated at one time. Collective runs are handled like V2 update modules.
### Resources
#website [Updates in the SAP System (BC-CST-UP) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/979cf1522d164bf7a781796efd8850ee/f334243e8f2b4e6fb9080b6c6a7ee41b.html?locale=en-US)
Transaction - SM13