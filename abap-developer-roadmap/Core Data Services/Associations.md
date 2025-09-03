#Basic 
Associations in SAP ABAP Core Data Services (CDS) are used to model semantically rich relationships between CDS view entities that closely align with business domain relationships. This is in contrast with traditional SQL joins which focus more on technical aspects rather than business semantics. 

```sql
define view ZI_Customer as select from I_Customer {
  key CustomerId,
  CustomerName,
  association [0..*] to I_SalesOrder as _Order on _Order.SoldToParty = CustomerId
}
```

CDS Associations define entity relationships including cardinality, ranging from one or zero 'to-one' to one or zero 'to-many' relationships. This provides metadata for design-time and run-time and makes the data model self-explaining and easier to understand. Associations can be exposed in view entities for navigation, directly accessed in to-one relationships, and used in WHERE clauses for filtering. Exposed associations allow navigation between related entities using path expressions. This is beneficial in OData services and SAP Fiori applications.

Defined associations automatically undergo query optimization at runtime. Amongst others join pruning occurs, i.e. should no fields of an associated entity be requested in a query then the join defined in the association will not be executed. General cardinality awareness, i.e. how many entities a join condition of an association will return, should be observed to ensure good performance. 

## Further reading

#Article [Defining Associations between CDS Entities](https://learning.sap.com/learning-journeys/acquire-core-abap-skills/defining-associations-between-cds-views_b325f87f-ff81-4bbe-a5c3-06d0c3ba5def)