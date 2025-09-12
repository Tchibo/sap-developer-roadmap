#intermediate 
### System Landscape Transformation 

**System Landscape Transformation (SLT)** is a data replication from a source system to a target database. Changes are recorded in the source database by database triggers and then replicated in a target database. 

Within SAP a change made to the source table is replicated into a staging table. This staging tables are processed by observer jobs running on the application server (not in the database)
reading all data for every entry and replicate it to a target database. 

### Smart Data Access
**Smart Data Access(SDA)** is a technology in SAP HANA that enables data federation by virtualizing remote data sources, allowing SAP HANA to access and query external databases as if their tables were local within HANA.

This requires additional effort since virtual database tables have to be made available via CDS table function, AMDP framework or via calculation views.

### Usage
Careful consideration must be given to the use of SDA & SLT for each use case, depending on the load generated to the database server, but also the redundancy and complexity added to the solution by the use of the respective technology.
### Resources
#website [Replicating Data to SAP HANA | SAP Help Portal](https://help.sap.com/docs/SAP_LANDSCAPE_TRANSFORMATION_REPLICATION_SERVER/007c373fcacb4003b990c6fac29a26e4/59eeabf5511d48d6b21326880fd58fd9.html?locale=en-US&q=System+Landscape+Transformation)
#website [SAP HANA Smart Data Access | SAP Help Portal](https://help.sap.com/docs/SAP_HANA_PLATFORM/6b94445c94ae495c83a19646e7c3fd56/a07c7ff25997460bbcb73099fb59007d.html?locale=en-US&q=smart+data+access)
