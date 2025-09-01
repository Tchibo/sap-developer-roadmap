#Basic 
Data Control Language (DCL) within ABAP Core Data Services (CDS) is SAP's authorization concept that offers declarative methods to enforce data access privileges directly at the data model level. Unlike conventional ABAP authorization, which targets transaction-level access, DCL enhances security by integrating it directly with data models, leading to a row-level "security by design." Making data access rules part of the virtual data model leads to a consistent authorization outcome across applications that are using the same CDS view entities.

DCL enforces authorization for data access at the database level by filtering unauthorized data before retrieval (row-level security). In this way DCL centralizes data access privileges while at the same time optimizing performance due to the reduced resultset size,  

DCL supports role definition using a syntax that designates the `select` operation with conditions defined using the `where` clause. The `pfcg_auth` function links DCL to SAP's Profile Generator authorization objects, adding another layer of security control.

```sql
@EndUserText.label: 'Access control for Sales Order'
@MappingRole: true
define role ZSalesOrderRole {
  grant 
    select
      on ZI_SalesOrder
        where
          ( SalesOrganization ) = aspect pfcg_auth( Z_SALES_ORG, Z_SALES_ORG, ACTVT = '03' );
}
```

DCL supports advanced features such as custom authorization aspects, session variables, and both instance-based and global authorizations, providing flexible security measures. In the SAP RESTful Application Programming Model (RAP), DCL automatically enforces access restrictions on OData services. 

## Further reading

#Article [Describing the authorization concept for ABAP CDS](https://learning.sap.com/learning-journeys/exploring-the-authorization-concept-for-sap-fiori-on-sap-s-4hana/describing-the-authorization-concept-for-abap-cds)