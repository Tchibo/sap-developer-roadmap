#intermediate 
REST (Representational State Transfer) is an architectural style for distributed systems which provides a uniform, resource-oriented interface via HTTP and is characterized by stateless communication, clear addressing and standardized methods such as GET, POST, PUT and DELETE.
### Usage
For Inbound scenarios where SAP provides data for a process or a user interface as backend OData should always be used. In outbound scenarios the usage of the implementation of a REST interface via `CL_REST_HTTP_CLIENT` in a custom development scenario should be carefully checked.
## Resources
#website[ABAP REST Library | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/753088fc00704d0a80e7fbd6803c8adb/2850217946b54e718e1f4afb35c4c283.html?locale=en-US)