#Intermediate 
Annotations in ABAP Core Data Services (CDS) semantically enrich CDS data definitions with metadata. Such metadata can provide business interpretations of the entity model, aid automatic user interface generation through Fiori Elements, configure search behavior for free text search, establish authorization controls for secure data access, play a role in analytics configuration for reporting and influence business object behavior in transactional processing.

The different categories of CDS annotations including UI, semantic, consumption, search, analytics, authorization and object model provide a comprehensive framework for reusable data models in SAP applications, allowing developers to meet requirements without extensive coding.

An annotation term in the CDS data definition is prefixed with '@' and can target the CDS view entity as a whole or individual entity elements. An entity or an entity element can each be annotated with more than one term.

```sql
@UI.headerInfo: {
  typeName: 'Sales Order',
  typeNamePlural: 'Sales Orders',
  title: { value: 'SalesOrderID' },
  description: { value: 'CustomerName' }
}
define view entity ZI_SalesOrder as select from zsalesorder {

  key SalesOrderID, 
  
  @ObjectModel.text.element: ['CustomerName']
  customer_id as CustomerID,
  
  @Semantics.amount.currencyCode: 'Currency'
  gross_amount as GrossAmount,
  
  @Semantics.currencyCode: true
  currency_code as Currency
}
```

By keeping UI annotations separate from CDS data definitions in so called metadata extensions the maintainability of SAP applications is enhanced. 

## Further reading

#Article [CDS Annotations](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/130e02a697e14bf8b05dd6672c56250b.html)