---
tags:
  - cds
  - data-modelling
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
In [[SAP Capire]], [[Views & Projections|projections]] and [[Views & Projections|views]] are key tools for shaping how data is presented and consumed by services.

**Projections** define service-specific interfaces on top of the core domain model. They expose only selected fields or aspects of an entity, ensuring internal data structures remain encapsulated while providing consumers or APIs with the necessary information. In a typical CAP project following the standard convention, projections are implemented in the `service.cds` file located in the `srv` folder of the application. This placement aligns projections with the service layer, keeping them separate from the core domain model defined in `schema.cds`.

**Views** are virtual entities that allow you to aggregate, filter, join, or transform data from one or more entities. They can be used to present derived or complex data structures without altering the underlying persistent tables. Views simplify queries and encapsulate business logic within the data model, making them reusable across different services or projections.

**Example**
```cds
// service.cds in the 'srv' folder
service CatalogService {
  // Projection exposing only selected fields
  entity Products as projection on my.Products {
    ID,
    name,
    price
  };
  
  // Internal view for aggregated data
  entity TopSellingProducts as select from my.Sales {
    product_ID,
    total: sum(quantity) as TotalSold
  } group by product_ID;
}
```

By defining projections and views in this way, CAP provides a clean separation between the persistent domain model and service-specific interfaces, improving maintainability, security, and clarity of the application logic.

**Sources**
- [SAP Capire - Views & Projections](https://cap.cloud.sap/docs/cds/cdl#views-projections)