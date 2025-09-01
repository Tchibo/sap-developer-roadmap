The SAP system uses a locking mechanism to ensure synchronized database access and to prevent parallel transactions from changing the same data at the same time. This locking concept is implemented by the Standalone Enqueue Server 2.

In an SAP transaction, enqueue locks are set when data is display and changed and can exist across several database LUWs. Database locks are much shorter. The difference between SAP LUW and database LUW relates to the functional scope of the update.

Another use case for locks is to set a lock when you want to ensure that a certain program only runs once at a time.
### Resources
[SAP Lock Concept | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/6568469cf5a1460a8d85c58b83d21ec2/47df116e6abf296fe10000000a42189b.html?locale=en-US)
Transaction Code - SM12
