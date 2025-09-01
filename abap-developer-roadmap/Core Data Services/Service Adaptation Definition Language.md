#Advanced 
The Service Adaptation Definition Language (SADL) is a component within the SAP technology stack in conjunction with ABAP Core Data Services (CDS) and the ABAP RESTful Application Programming Model (RAP). 

Despite being largely invisible to developers, SADL is an abstraction layer that translates OData requests into optimized ABAP SQL operations including caching and caters for integration between the CDS virtual data model and the OData service layer. SADL enhances developer productivity by automating SQL operations and  adapting to changes in underlying virtual data models without additional manual maintenance overhead.

Here is a bit more detail about what SADL contributes to processing of incoming OData requests for data in CDS managed virtual data models: 

* automatically transforms OData requests into ABAP SQL queries, which eliminates the need for developers to manually write SQL operations (like we used to have to do in the time of creating OData projects using transaction SEGW),
* SADL employs optimization techniques like predicate pushdown, efficient association handling, and paging optimization to ensure optimized SQL generation, 
* SADL interprets metadata annotations within CDS to influence query behavior and transaction management, including setting locks and performing authorization checks, 
* SADL manages standard operations for RAP business objects, like draft handling and ensures changes are made in controlled Logical Units of Work (LUW) 

## Further reading

#Article [Consuming Business Entities with SADL](https://help.sap.com/docs/ABAP_PLATFORM_NEW/7bfe8cdcfbb040dcb6702dada8c3e2f0/13d9849973dd4174adaa375f568984bf.html)
