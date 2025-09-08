The behavior implementation (an ABAP behavior pool) implements operations declared in the behavior definition (BDL). It executes whenever the RAP business object is accessed, whether from a Fiori app, OData web service, or ABAP code. 

The behavior implementation is a pool of local classes. There are two types of classes: handler classes (LHC) that implement of validations, determinations, feature and authorization control of an entity. The second type is the saver class (LSC) that controls the save sequence. In managed scenarios, the saver class is required only if custom persistence logic is needed.
Local classes and empty method implementations are generated automatically when invoked by  the Quick Assist (`CTRL + 1`).

#### Resources
- #website  [ABAP Behavior Pools (ABP) | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENABAP_BEHAVIOR_POOLS.html)
