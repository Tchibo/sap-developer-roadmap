The RFC gateway carries out RFC services based on TCP/IP. These services enable SAP systems and external programs to communicate with one another. (See Connectivity / RFC) Each application server instance of an ABAP system contains an RFC gateway. 

### Gateway Processes
The RFC gateway consists of the following processes:

- Gateway:
        The gateway process is started by the dispatcher and checked by this periodically. All RFC requests are received and processed by the gateway process.
- Gateway Monitor
        The gateway monitor is used for analysis and administration of the SAP Gateway. You can monitor the gateway with transaction SMGW.

### Resources
#website [RFC Gateway | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fbaae893ab3c486fb58bc18cfc01a543/48ace6623b1e35bae10000000a42189d.html?locale=en-US)
Transaction - SMGW