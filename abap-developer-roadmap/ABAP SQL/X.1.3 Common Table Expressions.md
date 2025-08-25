- create an temporary result set within a SQL select
- used with caution as the cannot be debugged and adds complexity
- use a separate CDS entity instead
**Common Table Expressions (CTEs)** are temporary, named result sets that can be utilized in an ABAP SQL statement.

```SQL
WITH +division_counts AS (
	SELECT  division,
			COUNT(*) AS productcount
	FROM i_product
	WHERE division IS NOT NULL
	GROUP BY division
)
SELECT  p~product,
		p~division,
		dc~productcount
FROM i_product AS p
INNER JOIN +division_counts AS dc
	ON p~division = dc~division
INTO TABLE @DATA(lt_product).
```


#### Resources
- #website [WITH, subquery_clauses | ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABAPWITH_SUBQUERY.html)
