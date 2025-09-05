The **bgRFC Framework (Background Remote Function Call Framework)** in SAP allows remote function calls to be executed asynchronously and in the background between different SAP systems or between a SAP system and a non-SAP system.
### Core Features
- Enables **asynchronous processing**, which ensures that the calling system is not blocked and can continue its operations while background processing occurs
- Guarantees **reliable transmission and execution** of remote function calls, providing **guaranteed delivery** between systems
- Ensures with **exactly once processing** that each unit of work is executed only a single time, thus preventing duplicate processing
- Offers **enhanced monitoring** capabilities, giving administrators better oversight and control compared to previous technologies like tRFC and qRFC, including advanced tools for tracking and managing queues and units.

### Resources
#website[bgRFC Architecture | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/753088fc00704d0a80e7fbd6803c8adb/489702b055493987e10000000a421937.html?locale=en-US)