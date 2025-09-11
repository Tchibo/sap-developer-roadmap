#Basic

SELECT statements in ABAP SQL handle data retrieval with built-in capabilities for filtering, sorting, and aggregating data. This functionality is known as Data Query Language (DQL).
Data from multiple tables can be combined using joins or ABAP CDS associations. Joins can also be performed with internal tables (table variables).

The **ABAP SQL Interface** converts ABAP SQL into the target database's SQL dialect (such as HANA SQL). When data is already cached in the AS ABAP table buffer, the **ABAP SQL engine** retrieves it directly from memory rather than making a database call.

Data received from SELECT statements can be stored in variables created by inline declaration `@DATA(lt_table)`.

```SQL
SELECT  product~ProductType,
		product~\_ProductType-ProductTypeCode,
		COUNT( * ) as NumberOfEntries
FROM I_Product as product
WHERE product~BaseUnit = 'KG'
GROUP BY product~ProductType,
		 product~\_ProductType-ProductTypeCode
ORDER BY NumberOfEntries
INTO TABLE @DATA(lt_product).
```

### Resources
- #website [ABAP SQL - Read Access with DQL | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENABAP_SQL_READING.html)
