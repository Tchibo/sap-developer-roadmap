#Advanced

With **ABAP Managed Database Procedures**, developers implement methods in **HANA SQLScript** that are called like any other ABAP method but run on the database (code pushdown). This gives access to HANA’s features and performance. AMDP methods are transported with their ABAP class and are automatically deployed to HANA on activation after import; they can be debugged with ADT. AMDP is limited to read-only access.

## Procedures and Functions

AMDP **Procedures** solve complex, multi-step tasks and offer finer control than ABAP SQL, including advanced hierarchy functions beyond ABAP CDS. AMDP **Functions** are useful to expose HANA objects from other schemas (e.g., via Smart Data Access) or DB objects such as Calculation Views to ABAP.

## When to use

If a task can be solved well in ABAP, prefer ABAP for maintainability and portability. ABAP is widely understood and easier to debug, whereas SQLScript is a separate skill.
Reserve AMDP for cases where pushdown is required for **performance** or when **very large result sets** would otherwise be transferred to the ABAP stack only to be filtered later or if you need to access data from other schemas.
Do consider CDS table functions backed by Calculation Views with a minimal amount of AMDP code for complex selections.

# Resources
#website [ABAP Managed Databse Procedures](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/abap-managed-database-procedures-amdp)
#course [Create an ABAP Managed Database Procedure (AMDP) and Analyze Its Performance](https://developers.sap.com/tutorials/abap-environment-amdp-profiling.html)