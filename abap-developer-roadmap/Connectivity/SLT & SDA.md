### System Landscape Transformation 
- [ ] Hier könnte noch die Info rein, dass das ein Tool des ABAP Application Server ist und die Daten von dort migriert werden.
System Landscape Transformation (SLT) is a data replication from a source system to a target database.

Changes are recorded in the source database by database triggers and then replicated in a target database. In SAP, this is done by a trigger that updates the keys of the object to a staging table after a change to a DB table. From there, they are updated to the target database by a replication job on the application server.

### Smart Data Access
- [ ] Hinzufügen?: To access a virtualized database table in ABAP, they must be made available via a CDS table function and the ABAP AMDP framework.
**Smart Data Access(SDA)** is a technology in SAP HANA that enables data federation by virtualizing remote data sources, allowing SAP HANA to access and query external databases as if their tables were local within HANA.
### Usage
Careful consideration must be given to the use of SDA & SLT for each use case, depending on the load generated to the database server, but also the redundancy and complexity added to the solution by the use of the respective technology.
### Resources
#website [Replicating Data to SAP HANA | SAP Help Portal](https://help.sap.com/docs/SAP_LANDSCAPE_TRANSFORMATION_REPLICATION_SERVER/007c373fcacb4003b990c6fac29a26e4/59eeabf5511d48d6b21326880fd58fd9.html?locale=en-US&q=System+Landscape+Transformation)
#website [SAP HANA Smart Data Access | SAP Help Portal](https://help.sap.com/docs/SAP_HANA_PLATFORM/6b94445c94ae495c83a19646e7c3fd56/a07c7ff25997460bbcb73099fb59007d.html?locale=en-US&q=smart+data+access)
