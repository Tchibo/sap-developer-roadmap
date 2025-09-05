ABAP SQL offers a wide range of built-in functions for numeric operations, string manipulation, date and time handling, type conversions, and additional data processing tasks.

Additionally, ABAP SQL provides a set of keywords like CASE or CAST to process data elements.
```SQL
SELECT  ROUND( NetWeight, 0 ) as NetWeightKg,
		CONCAT( Division, Brand ) as Combined,
		CASE WHEN ProductGroup = '1' THEN @abap_true
			 ELSE @abap_false END AS ProductGroupOne,
		DAYS_BETWEEN( CreationDate, @sy-datum ) as ProductLiveTime
FROM I_Product
WHERE BaseUnit = 'KG'
```
### Resources
- #website [DDIC - Built-In Functions | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABENDDIC_BUILTIN_FUNCTIONS.html)