#intermediate 
Within SAP different types of work processes (wp) exist in which requests are executed. This can be seen in transaction SM51 or SM66 in the column work process type. 

Work processes can also be configured out in different quantities depending of day or night work mode. So during day time you might have higher quantities of dialog wp's and during night time higher quantities of batch wp's.

Dialog wp's (type DIA) are use to deal with all requests triggered by an active user (person or program) as well as all non-specialized requests that, for example, are received from RFC and HTTP connections. 

Update wp's  (type UPD & UPD2) are used to lighten the workload of the SAP transactions when time-consuming changes are made to the database. The updates are then carried out asynchronously in special updating work processes. 

Batchprocessing wp's (type BTC) are used by programs that can be executed without user interaction, with the Computing Center Management System (CCMS) in background processing. (see Background Processing)

Print wp's (type SPO) are used for administration and processing of spool requests.

Enqueue wp's are used for Lock and Releasing locks on business objects (see Lock Server).
### Resources
#website [Updates in the SAP System (BC-CST-UP) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/979cf1522d164bf7a781796efd8850ee/f334243e8f2b4e6fb9080b6c6a7ee41b.html?locale=en-US)
#website [Background Processing | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/b07e7195f03f438b8e7ed273099d74f3/4b26e702f89c74fee10000000a421937.html?locale=en-US)
#website [SAP Printing Guide (BC-CCM-PRN) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/290ce8983cbc4848a9d7b6f5e77491b9/4ea6932d50ba25d0e10000000a421937.html?locale=en-US)