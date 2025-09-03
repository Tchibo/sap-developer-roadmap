---
tags:
  - cds
  - data-modelling
  - revisit
  - cap-cds
  - basic
links:
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/guides/domain-modeling#views-projections
aliases:
  - view
  - views
  - projection
  - projections
---
In [[SAP Capire]], [[Views & Projections|projections]] and [[Views & Projections|views]] are powerful modeling tools that allow developers to shape how data is presented and consumed.

**Projections** are used to define service-specific interfaces on top of core domain models. By creating projections, you can expose only selected fields and aspects of an entity to a service, ensuring that internal data structures remain encapsulated and that only the necessary data is available to [[API]]s or consumers. Projections enable a clear separation between internal domain models and external service contracts, which is important for maintainability and security.

**Views** in [[SAP Capire]] are virtual entities defined with SQL-like queries. Views allow you to aggregate, filter, join, or transform data from one or more entities to present complex or derived data structures as reusable parts of your model. Views help to simplify queries and encapsulate business logic within the data model, making it easier to work with complex requirements without changing the underlying persistent entities.

**Example**
```cds
// A projection for an external service
service CatalogService {
  entity Products as projection on my.Products {
    ID,
    name,
    price
  };
}

// A view for internal use
entity TopSellingProducts as select from my.Sales {
  product_ID,
  total: sum(quantity) as TotalSold
} group by product_ID;
```

**Summary**  
Projections in [[SAP Capire]] define service-specific interfaces, exposing only necessary data fields to consumers. Views are virtual entities that transform, aggregate, or join data for internal processing. Both concepts support clean data modeling and flexibility in [[SAP Capire]] applications.

**Sources**
- [SAP Capire - Views & Projections](https://cap.cloud.sap/docs/cds/cdl#views-projections)