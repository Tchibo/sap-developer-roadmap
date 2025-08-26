**Common Table Expressions (CTEs)** are temporary named result sets in ABAP SQL. They work like temporary views that allow you to combine multiple SELECT operations within a single ABAP SQL statement.
The `WITH` statement allows you to define CTEs using the syntax `<cte_name> AS ( <cte_select_statement>)`, which can then be joined with the main SELECT statement.

Use CTEs cautiously as you cannot examine their intermediate results in the debugger. Before implementing a CTE, consider alternatives such as creating reusable ABAP CDS views or storing intermediate results in internal tables for better maintainability. CTEs are most appropriate when processing large datasets that should remain at the database level rather than being transferred to the ABAP application server to optimize performance and memory usage.

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
