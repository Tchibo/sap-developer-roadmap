
> [!open]+ Vorschlag 1
> For supported standard business objects, no custom outbound implementation is required because SAP provides it. DRF customizing is performed in the source system via transaction DRFOUT.

- [ ] Ich hadere ein bisschen damit Master data mit SAP Standarddaten gleichzusetzen. 
- [ ] Customizing würde ich hier oben rausnehmen. Unten ist es gut erwähnt.
	- [ ] sollten wir mal zu sprechen - tu mich mit dem Punkt grade schwer

=> Check mit Edna

The Data Replication Framework (DRF) provides the ability to replicate master data as well as  customizing from one SAP system to another. The replication can either be done as full replication or as delta replication which is then based on change data capture methods within SAP.

DRF decouples the replication from the transmission method offering the possibility to use different transmission channels (e.g., IDoc, SOAP, RFC with BAPI). Also filtering can be either customized or implemented as well as other parameters like parallelization or language dependency of the distribution. 
### Usage
DRF should be used in distribution scenarios, where standard business objects need to be distributed and standard technologies for distributions are available. This applies for IDocs as well as SOAP Services, the options RFC and File should be avoided.

It should also be mentioned that the replication does not react to an event / change pointer at a precise point in time, but starts via a scheduled job and is therefore more suitable for integration requirements that do not require the provision of data at a precise point in time such as master data.

Custom implementations within DRF are possible but should be checked carefully regarding the requirements of the integration scenario. 
### Resources
#website[Data Replication Framework | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/8308e6d301d54584a33cd04a9861bc52/88e3f5577c84bc12e10000000a4450e5.html?locale=en-US)
Replication Control - Transaction DRFOUT
Customizing DRF - Transaction DRFIMG