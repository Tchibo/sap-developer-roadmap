#Intermediate 
Entity projections in ABAP Core Data Services (CDS) are created based on an underlying interface view entities and used to create view entities of CDS data models that are tailored to specific business applications. Projections are meant to shield applications from the complex underlying data model and ensure stable interfaces despite changes in base entities. Entity projections enable developers to rename and transform fields and, by restricting fields from existing CDS entities, to enhance performance by limiting data transfer to just the necessary fields and records. 

Entity projections are created in the context of analytical queries for consumption in analytical tools like SAP Analytics Cloud or in the context of the RESTful Application Programming Model (RAP) for transactional consumers, i.e. APIs or Fiori Elements apps that modify data. By naming convention Projection entities are prefixed with ZC_ ('C' for Consumption).

For an analytical query the projection is created as a transient view entity with provider contract 'analytical_query'. In RAP projections are created with provider contract 'transactional_query' for all view entites that form part of the RAP business object. Projected view entities are exposed in Service Definitions for OData consumption in APIs, Fiori Applications or analytical Tools.

The following defines an entity projection as 'transactional query' for a RAP business object. 

```sql
@EndUserText.label: 'Sales Order Projection View'
@AccessControl.authorizationCheck: #CHECK
@Metadata.allowExtensions: true
define root view entity ZC_SalesOrder 
  provider contract transactional_query
  as projection on ZI_SalesOrder {
  key SalesOrderID,
      CustomerID,
      OrderDate,
      @Semantics.amount.currencyCode: 'Currency'
      GrossAmount,
      Currency,
      /* Associations */
      _Items : redirected to composition child ZC_SalesOrderItem,
      _Customer
}
```

## Further reading

#Article [Projection Views](https://help.sap.com/docs/abap-cloud/abap-data-models/cds-projection-views)
#Article [Describing the role of an analytical projection view](https://learning.sap.com/learning-journeys/developing-analytical-queries-using-abap-core-data-services/describing-the-role-of-a-cds-analytical-projection-view)
#Article [Transactional Queries](https://help.sap.com/docs/abap-cloud/abap-data-models/cds-transactional-queries)
