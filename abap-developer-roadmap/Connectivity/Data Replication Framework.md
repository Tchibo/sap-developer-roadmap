- [ ] Vorschlag 1
- [ ] No images allowed - sorry
- [ ] Kann man das auch für Z-BOs verwenden? Bzw. Lohnt es sich, dafür zu Implementieren oder sollte man dann eine neuere Technologie nehmen?
- [ ] Was ist mit Alternativen wie MDG, MDI? In Usage erwähnen?
> [!open]+ Vorschlag 1
> The Data Replication Framework (DRF) is a tool for replicating the master data of standard business objects (e.g., Business Partner) from one system to another. DRF replication is independent of the transmission technology (e.g., IDoc, SOAP, RFC with BAPI).
> 
>For supported standard business objects, no custom outbound implementation is required because SAP provides it. DRF customizing is performed in the source system via transaction DRFOUT.

The Data Replication Framework (DRF) provides the ability to replicate most of the business objects and there assignments by the use of standard content. 

![[Pasted image 20250829091128.png]]

The outbound implementation defines the business object that will be distributed as well as the used communication channel and the target system. Additional parameters can be applied for parallelization or language dependency of the distribution. 

Either a complete full load of an object can be sent, e.g. for customizing, or deltas can be derived from existing change triggers and distributed.

### Usage
DRF should be used in distribution scenarios, where standard business objects need to be distributed and standard technologies for distributions are available. This applies for IDocs as well as SOAP Services, the options RFC and File should be avoided.

It should also be mentioned that the replication does not react to an event / change pointer at a precise point in time, but starts via a scheduled job and is therefore more suitable for integration requirements that do not require the provision of data at a precise point in time such as master data.

### Resources
[Data Replication Framework | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/8308e6d301d54584a33cd04a9861bc52/88e3f5577c84bc12e10000000a4450e5.html?locale=en-US)