> [!todo] Handler- and Saver local classes, entity type derived types
> - [x] Do mention a.) hat the implementation in local classes of the behaviour pool occurs in a handler and a saver class per entity type of the behaviour definition and that 
> 	- [x] Added.
> - [x] b.) method stubs are created based on behaviour definition with a signature of entity type derived types. 

The behavior implementation (an ABAP behavior pool) implements operations declared in the behavior definition (BDL). It executes whenever the RAP business object is accessed, whether from a Fiori app, OData web service, or ABAP code. 

The behavior implementation is a pool of local classes. There are two types of classes: handler classes (LHC) that implement of validations, determinations, feature and authorization control of an entity. The second type is the saver class (LSC) that controls the save sequence. In managed scenarios, the saver class is required only if custom persistence logic is needed.
Local classes and empty method implementations are generated automatically when invoked by  the Quick Assist (`CTRL + 1`).

#### Resources
- #website  [ABAP Behavior Pools (ABP) | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENABAP_BEHAVIOR_POOLS.html)
