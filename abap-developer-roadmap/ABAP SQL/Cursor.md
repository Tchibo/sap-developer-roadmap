A cursor is a mechanism for processing large datasets by dividing them into manageable portions that can be handled sequentially. 

When a cursor is created, the database executes the query but keeps the complete result set on the database side. It maintains a pointer (called a cursor) to track the current position and delivers only the requested data chunk to the application server per fetch. This approach reduces memory usage on the application server.

Cursors consume resources on the database session while being processed, because the database maintains the cursor position and associated resources. If a cursor is not properly closed,  database resources are not freed (until the next commit). The number of open cursors per database session is capped so as not to overburden the database.

Another construct that uses an implicit database cursor is the `SELECT … ENDSELECT` loop.
#### Usage
Only use cursors when you process huge datasets that cannot be fetched at once. Review alternatives like HANA calculation views or CDS table functions with AMDP. If you use cursors to improve performance when looping through internal tables, use sorted tables instead.

> [!NOTE] Anmerkung Nico
>Ich stelle die grundsätzliche Nutzung von Cursor mal infrage. Wenn man einen Cursor nutzt, ist das aus meiner Sicht ein architektonischer Fehler - zumindest fällt mir kein Use Cases ein wo man so etwas brauchen sollte. Insofern lasse ich das mal unangetastet / überlasse Hendrik die finale Entscheidung über drin oder raus lassen. Aber aus meiner Sicht wiederspricht Cursor dem Prinizip der Minimalisierung des Austausches zwischen App und DB Server..

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
