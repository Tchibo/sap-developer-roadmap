#Basic 
ABAP Core Data Services (CDS) offer a data modelling framework tailored for SAP applications, utilizing a Data Definition Language (DDL) that enhances traditional SQL capabilities. Its SQL-like syntax is intuitive for ABAP developers, facilitating the definition of CDS entities through a declarative approach. 

The basic structure involves defining views using the `SELECT` statement to specify fields sourced from database tables. Developers can select fields directly, apply calculations, rename fields using aliases, and designate primary keys using the `key` keyword, reflecting a flexible syntax for data manipulation.

```sql
define view CustomerView as select from Customers {
    key ID,
	    Name,
	    Address,
	    Revenue + Tax as TotalAmount
}
```

CDS enables data operations through various `JOIN` types: inner join for matching records from multiple tables, left outer join for retrieval from primary tables, and cross join for Cartesian product generation. Additional SQL elements include the `WHERE` clause for condition-based filtering, `UNION` for combining query results, and `GROUP BY` for data aggregation, paired with the `HAVING` clause for conditional aggregation filtering. Sorting is achieved with `ORDER BY`, while `LIMIT` and `DISTINCT` manage record volumes and uniqueness, respectively.

```sql
define view OrderDetails as select from Orders 
    inner join Products on Orders.ProductID = Products.ID {
    Orders.ID as OrderID,
    Orders.Date,
    Products.Name as ProductName,
    Products.Price
}
```

Beyond SQL, CDS incorporates associations for modeling relationships between entities, fostering enhanced data structuring. Ultimately, CDS DDL empowers developers to construct sophisticated virtual data models foundational to SAP applications, promoting optimized performance and maintainability.

## Further reading

#Article [How ABAP CDS relates to SQL](https://help.sap.com/docs/abap-cloud/abap-data-models/roots-sql)
