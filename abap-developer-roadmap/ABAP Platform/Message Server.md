#intermediate 
There is only one SAP Message Server in every ABAP system, which runs as part of the ABAP Server Central Services instance.

It performs the following tasks in the ABAP system:
- Central communication channel between the individual AS instances of the system
- Load distribution of logons using SAP GUI and RFC with logon group    
- Information point for the SAP Web Dispatcher and the AS instances (each AS instance of the system firsts logs on to the message server)

When an instance is started, the dispatcher process reports its services to the message server. If the message server fails, it must be restarted as quickly as possible to ensure trouble-free operation.
#### Resources
#website [SAP Message Server | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/77b3972f873044acb3a70258f3984c64/47c2e77bb8fd3020e10000000a42189d.html?locale=en-US)
Transaction - SMLG (Load Distribution / Logon Groups)