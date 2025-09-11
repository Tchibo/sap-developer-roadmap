#Basic #Topic3

Structured data types such as structures and tables. Structures group related fields together. Internal tables are dynamic arrays of structures or elementary types, widely used for collections of data.
# Structures
A Structure is an aggregation of multiple data types. It can contain elementary data types, other structures or table types.
```abap
TYPES: BEGIN OF STRUCTURE struct,
         field1 TYPE i,
         field2 TYPE matnr,
       END OF STRUCTURE struct.
```
# Table Types
Tables store data as variable-length sequences of identical **Line Types** (Data Elements, Structures, or Reference Variables). The **Table Category** determines management and storage: **`STANDARD`** tables are write-optimized and require no key. **`SORTED`** tables are read-optimized with unique/non-unique **Table Keys**. **`HASHED`** tables provide constant read/write speed for large datasets using hashed keys but don't support sequential iteration.

```abap
TYPES tab TYPE STANDARD TABLE OF struct WITH EMPTY KEY.
```

## Range Tables
A **range table** is a specialty in the SAP ecosystem. It is an internal table with a specific structure (fields SIGN, OPTION, LOW, and HIGH) that allows you to define complex selection criteria for filtering data. In ```LOOP...WHERE``` or ```SELECT...WHERE```, conditions from Range Tables are OR-linked.
```abap
TYPES: range_table TYPE RANGE OF matnr.
```
### Resources
#website [SAP Help for Cloud: Table Types](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENITAB_DATA_TYPE.html)
#article[ABAP Cheat Sheets | Table Types](https://github.com/SAP-samples/abap-cheat-sheets/blob/main/01_Internal_Tables.md)
#article [Technical differences of the table types (standard, sorted, hashed)](https://sapr3.weebly.com/abap/-standard-tables-vs-sorted-table-vs-hashed-tables)
#video [YouTube | Create Range Tables in SAP ABAP ](https://www.youtube.com/watch?v=eq0wH09xk24)
#website[SAP Help for Cloud: Structures](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENDDIC_STRUCTURES.html)