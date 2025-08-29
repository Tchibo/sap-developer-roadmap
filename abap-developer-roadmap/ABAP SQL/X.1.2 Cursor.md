When you process large data sets, it can be helpful to slice the data is workable slices and process them one after the other. This is what a cursor does. You can create a cursor for a certain select and fetch chunk by chunk of that data in a loop and process it.
An ABAP cursor creates a cursor on the database. The database processes the according query but does not return the result. Instead it holds a pointer (cursor) to the current position and returns the requested chunk of data.
This reduces the data that has to be cached in the application server at the time. But it also results in multiple selects to the database.
Cursor is sometimes used to process entry by. This results in a lot of database traffic. only use for big datasets. 

It is important to Close a cursor after processing 

- OPEN CURSOR versus SELECT + ENDSELECT
- parallel processing ?


**How it Works:**
```
" 1. Open the cursor (place your bookmark)
OPEN CURSOR @cursor FOR SELECT * FROM huge_table WHERE...

" 2. Read data in chunks (read a few pages at a time)
DO.
  FETCH NEXT CURSOR @cursor INTO TABLE @lt_data PACKAGE SIZE 1000.
  IF sy-subrc <> 0.
    EXIT. " No more data (reached the end of the book)
  ENDIF.
  
  " Process your 1000 records here
  LOOP AT lt_data INTO ls_data.
    " Do something with each record
  ENDLOOP.
ENDDO.

" 3. Close the cursor (remove your bookmark)
CLOSE CURSOR @cursor.
```


#### Resources
- #website [OPEN CURSOR](https://help.sap.com/doc/abapdocu_751_index_htm/7.51/de-de/abapopen_cursor.htm)
