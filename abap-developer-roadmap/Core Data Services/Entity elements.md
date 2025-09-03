#Basic 
Entity elements in ABAP Core Data Services (CDS) represent the individual data points within CDS entities. These elements can be directly sourced from database tables, calculated on-the-fly using formulas or aggregated from the data source. Understanding the different available types of entity elements, including persisted, calculated, virtual, association-based, aggregated, and redirected, allows developers to take advantage of CDS's features for modeling semantically rich virtual data models.

* **Persisted** elements map directly to physical database fields, offering high-performance data access for standard retrieval tasks. 
  
* **Calculated** elements derive their values dynamically at runtime using expressions, allowing for real-time data transformation and business logic application without physical storage. 
  
* **Virtual** elements support parameter fields and transient data not directly mapped to database fields, enabling customizable and flexible queries. 
  
* **Association-based** elements facilitate direct access to related fields in other entities, simplifying relationship modeling and integration. Note though that association based fields 'materialize' the join that is expressed in the association definition, i.e. join pruning is no longer carried out even if the association based field is not requested. Use sparingly as it has an impact on performance. 
  
* **Aggregated** elements result from grouping and aggregating functions, providing summarized information critical for analytical applications. Redirected elements allow reuse of existing field definitions, centralizing maintenance and promoting consistency across CDS entities. Enhancing these elements with annotations — such as semantic, UI, and search annotations — further enriches their functionality.

## Further reading

#Article [CDS View Entity SELECT element](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENCDS_SELECT_LIST_ENTRY_V2.html)
