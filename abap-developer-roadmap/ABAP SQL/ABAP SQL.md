ABAP SQL (formerly known as Open SQL) is a specialized SQL variant designed for ABAP programming. Its main goal is to streamline database interactions from ABAP application servers while providing **database independence**.

```SQL
SELECT * FROM I_Product
WHERE BaseUnit = 'KG'
ORDER BY Product ASCENDING
INTO TABLE @DATA(lt_product).
```

ABAP SQL can only interact with database objects that have corresponding ABAP representations. For SAP HANA-specific objects like calculation views, accessibility must be established through AMDP (ABAP Managed Database Procedures) and CDS table functions.

ABAP SQL supports full CUD (Create, Update, Delete) functionality. This subset of ABAP SQL commands is called Data Manipulation Language (DML).
```SQL
DELETE FROM ztable WHERE product = '123'.
```

> [!NOTE] Vorschlag einheitliche Formulierung -startend mit einem Verb / ohne "man sollte"
> Modern ABAP development follows specific best practices with certain limitations:
> - **Read Operations**: Utilize ABAP CDS views rather than querying database tables. 
>- **Write Operations**: Manage Create, Update, and Delete operations through RAP (RESTful ABAP Programming) entities instead of direct execution.
>- **Performance**: Keep database access efficient by reducing both the frequency of calls and the volume of data requested. For example, avoid SELECT statements in loops and only retrieve the specific fields you need. 
>- **Clean Core**: Use existing standard CDS and business object interfaces to access Standard Business Objects.

Modern ABAP development follows specific best practices with certain limitations:
- **Read Operations**: Should utilize ABAP CDS views rather than querying database tables directly.
- **Write Operations**: Create, Update, and Delete operations should be managed through RAP (RESTful ABAP Programming) entities instead of direct execution.
- **Performance**: Keep database access efficient by reducing both the frequency of calls and the volume of data requested. For example, avoid SELECT statements in loops and only retrieve the specific fields you need. 
- **Clean Core**: Use existing standard CDS and business object interfaces to access Standard Business Objects.

### Resources   
- #website [ABAP SQL | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENABAP_SQL.html)