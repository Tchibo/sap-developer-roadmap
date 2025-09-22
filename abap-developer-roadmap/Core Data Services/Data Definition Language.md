#Basic 
The Data Definition Language (DDL) in Core Data Services (CDS) is used to define data models with entity relationships for the use in analytical or transactional applications, e.g. as the basis of business objects in the RESTful ABAP Programming model (RAP) or analytical queries for use in reporting. DDL supports a declarative approach to data modeling, promoting consistency and reuse across various application layers.  

Key features of DDL include the ability to define e.g. CDS tables, view entities and custom entities and their relationships in the form of associations and to leverage annotations. Activating a DDL view entity defnition, possibly with associations, creates a view on the database and leads to optimized SQL execution plans for data retrieval. Using DDL to define data models thus promotes the code-push-down to the database to alleviate load on the application server.

```sql
define view entity ZI_FlightWithCarrier as select from sflight
  association [0..1] to ZI_Carrier as _Carrier on $projection.carrid = _Carrier.carrid {
    key sflight.carrid,
    key sflight.connid,
    _Carrier.carrname
}
```

DDL annotations allow to provide metadata that enriches the data model for various use cases like the generation of Fiori Elements UIs, rendering in OData services and analytical queries. These annotations help optimize data models for specific runtime contexts.

## Further reading

#Article [ABAP CDS DDL for data definitions](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENCDS_F1_DDL_SYNTAX.html)
#Article [Naming conventions in the virtual data model](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/ee6ff9b281d8448f96b4fe6c89f2bdc8/8a8cee943ef944fe8936f4cc60ba9bc1.html)
#Article [ABAP CDS Annotations](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENCDS_ANNOTATIONS.html)

