> [!todo] More RAP technical details
>  - [ ] In addition to the semantic description of a BO add some RAP technical detail about how a BO is implemented, i.e. view entity composition, entity projection with provider contract, behaviour definition and projection and behaviour implementation
> 	 - [ ] I'd like to stick to the business concept here. I go into more detail in other articles. 

A Business Object (BO) is a hierarchical, structured representation of a real-world business entity that combines related data and operations within a specific business context. It contains both data and logic for particular business cases, including validations and BO-specific actions required for enterprise application development.

For example, a Sales Order business object aggregates sales order header data with its line items in a hierarchical structure. It provides explicit behaviors and operations such as "order placed" (create), "order withdrawn" (delete), and "order delivered" (update).

The hierarchical structure and lifecycle management are implemented through a specific relationship type called **composition**.

### Resources
- #website[Business Object | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/a3ff9dcdb25a4f1a9408422b8ba5fa00.html?locale=en-US)