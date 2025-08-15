ABAP has built-in data types found in both its **language** and the **ABAP Dictionary**. This section covers the language data types, while those in the ABAP Dictionary are addressed separately.
# Built-In Data Types
Fixed predefined datatypes like `c` (character), `n` (numeric character), `i` (integer), `p` (packed decimal), and `f` (floating-point). These are mostly used for scalar values and simple fields.

Every ABAP type has enforced byte length and format, influencing storage and how content is processed.
- Character types (e.g., `c`, `string`) handle text, while numeric types (`n`, `i`) represent numbers with distinct characteristics.
- Special types `d` (date), `t` (time) and `utclong` (timestamp) follow SAP’s standard formatting: `YYYYMMDD`, `HHMMSS` and POSIX-standard UTC timestamps, respectively.
# Reference Data Types
Types that refer to objects or data, for example, `REF TO <class/interface>` and `REF TO <type>`. These provide pointers to ABAP objects or data areas. Using pointers instead of value variables can be beneficial for performance and reduce runtime storage requirements.

## Field-Symbols
Field Symbols are a precursor to reference data types but still required in modern ABAP. In all cases where both field-symbols and reference data types are possible, reference data types are preferred. Field-Symbols are commonly used in FOR constructor expressions:

```abap
DATA(itab2) = VALUE table_type(FOR <field-symbol> IN itab1
	( VALUE #( BASE <field-symbol> demo_attr = abap_true ) ) ).
```

# Generic Types

Generic Types are commonly used in **Dynamic Programming** in **Advanced ABAP**. #todo topic dynamic programming unter "Advanced ABAP".

#### Links
#website[ABAP Built-In Types](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/index.htm?file=abenbuilt_in_types_complete.htm)
#website [Generic ABAP Types](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/index.htm?file=abenbuilt_in_types_generic.htm)
#article [Explore Data Type Conversions with 30 Examples](https://community.sap.com/t5/technology-blog-posts-by-members/sap-abap-explore-data-type-conversions-with-30-examples/ba-p/13968953)