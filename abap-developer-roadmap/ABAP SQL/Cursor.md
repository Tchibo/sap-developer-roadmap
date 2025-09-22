#Advanced 

A cursor is a mechanism for processing large datasets by dividing them into manageable portions that can be handled sequentially. 

When a cursor is created, the database executes the query but keeps the complete result set on the database side. It maintains a pointer (called a cursor) to track the current position and delivers only the requested data chunk to the application server per fetch. This approach reduces memory usage on the application server.

Cursors consume resources on the database session while being processed, because the database maintains the cursor position and associated resources. If a cursor is not properly closed,  database resources are not freed (until the next commit). The number of open cursors per database session is capped so as not to overburden the database.

Another construct that uses an implicit database cursor is the `SELECT … ENDSELECT` loop.
#### Usage
Cursors should generally not be used in ABAP anymore. Double-check your application design before reading large amounts of data. If large-scale processing is still required, consider code pushdown technologies such as ABAP CDS, SAP HANA calculation views, or CDS table functions implemented with AMDP.

```ABAP
DATA lt_product TYPE TABLE OF I_Product.

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

### Resources
- #website [OPEN CURSOR - ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_753_index_htm/7.53/en-US/abapopen_cursor.htm)
- #website [ENDSELECT - ABAP Keyword Documentation](https://help.sap.com/doc/abapdocu_753_index_htm/7.53/en-US/abapendselect.htm)
