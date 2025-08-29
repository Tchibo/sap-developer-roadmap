<<<<<<< HEAD
A cursor is a mechanism for processing large datasets by dividing them into manageable portions that can be handled sequentially. 
=======
> [!NOTE] Vorschlag
>For processing large data sets on the application server the concept of cursors exists. Basically a request  to the database is needed that would return too much data to process at once. Therefore the data is requested in slices and only the slices are processed. The cursors marks the psotion of the next slice and allows to read further from the database.

When you process large data sets, it can be helpful to slice the data in workable slices and process them one after the other. This is what a cursor does. You can create a cursor for a certain select and fetch chunk by chunk of that data in a loop and process it.

An ABAP cursor creates a cursor on the database. The database processes the according query but does not return the result. Instead it holds a pointer (cursor) to the current position and returns the requested chunk of data.

This reduces the data that has to be cached in the application server at the time. But it also results in multiple selects to the database.

Cursor is often used to process entry by. This results in a lot of database traffic. Only use cursor for big datasets. If you want to improve performance, check if you can use sorted tables instead.
>>>>>>> 3e56082206a0a628079775d03eaa8524b3ea40e1

When a cursor is created, the database executes the query but keeps the complete result set on the database side. It maintains a pointer (called a cursor) to track the current position and delivers only the requested data chunk to the application server per fetch. This approach reduces memory usage on the application server.

Cursors consume resources on the database session while being processed, because the database maintains the cursor position and associated resources. If a cursor is not properly closed,  database resources are not freed (until the next commit). The number of open cursors per database session is capped so as not to overburden the database.

<<<<<<< HEAD
Another construct that uses an implicit database cursor is the `SELECT … ENDSELECT` loop.
#### Usage
Only use cursors when you process huge datasets that cannot be fetched at once. Review alternatives like HANA calculation views or CDS table functions with AMDP. If you use cursors to improve performance when looping through internal tables, use sorted tables instead.

```ABAP
DATA lt_product TYPE TABLE OF I_Product.
=======
> [!NOTE] Vorschlag
>### Usage
>The cursor concept is an relatively old concept but still used within ABAP. Before using this possibility it should be always checked if its the right concept to provide data in mass quantity / what are the real application needs.


### Example
```
" 1. Open the cursor (place your bookmark)
OPEN CURSOR @cursor FOR SELECT * FROM huge_table WHERE...
>>>>>>> 3e56082206a0a628079775d03eaa8524b3ea40e1

OPEN CURSOR @DATA(cursor) FOR
    SELECT Product FROM I_Product WHERE PackagingMaterialGroup = 'WERT'.
DO.
  FETCH NEXT CURSOR @cursor INTO TABLE @lt_product PACKAGE SIZE 1000.
  IF sy-subrc <> 0.
    EXIT. " No more data (reached the end of the result set)
  ENDIF.

  LOOP AT lt_product INTO DATA(ls_product).
    " Do something with each record
  ENDLOOP.
ENDDO.

" 3. Close the cursor (free database connection and memory)
CLOSE CURSOR @cursor.
```

``` ABAP
SELECT Product FROM I_Product WHERE ProductCategory = '00'
  INTO TABLE @DATA(lt_product) PACKAGE SIZE 100.

  LOOP AT lt_product ASSIGNING FIELD-SYMBOL(<ls_product>).
    " Process each product record
  ENDLOOP.
ENDSELECT.
```

#### Resources
- #website [OPEN CURSOR - ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_753_index_htm/7.53/en-US/abapopen_cursor.htm)
- #website [ENDSELECT - ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_753_index_htm/7.53/en-US/abapendselect.htm)
