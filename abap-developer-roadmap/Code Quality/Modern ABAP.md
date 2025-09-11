#Basic 

Modern ABAP features promote code that is clean, efficient, and maintainable and adheres to Clean ABAP principles for human readability. Using the following ABAP features amongst others makes your code benefit from fewer data declarations and conditional statements. 

- **Inline Data Declaration**: Allows variable declaration within the statement where they are first used, enhancing code conciseness and readability.

```
DATA(lv_number) = 42.
```


- **String Templates**: Facilitate efficient and intuitive string operations by embedding expressions within strings for improved readability and dynamic integration.

``` 
DATA(lv_text) = 
|Hallo { sy-uname }!{ cl_abap_char_utilities=>newline }|  && 
|Heute ist { sy-datum DATE = ISO } um { sy-uzeit TIME = ISO }.|.       
```    


- **Table Expressions**: Offer advanced internal table handling, employing expressions like `FOR`, `REDUCE`, and `FILTER` to streamline data operations; ensuring compact transformations and efficient execution.

```
DATA(nums) = VALUE TABLE OF i( FOR n = 1 UNTIL n > 3 ( n ) ).
```

```
DATA(sum) = REDUCE i( INIT s = 0 FOR n = 1 UNTIL n > 5 NEXT s = s + n ).
```

```
DATA lt_spfli TYPE STANDARD TABLE OF spfli WITH EMPTY KEY.

SELECT * FROM spfli INTO TABLE @lt_spfli UP TO 10 ROWS.

DATA(lt_lh) = FILTER #( lt_spfli WHERE carrid = 'LH' ).
```


- **Constructor Expressions**: Leverage expressions like `VALUE`, `CORRESPONDING`, `COND`, and `SWITCH` for data object creation. These enhance code clarity, promote simplified data mappings and transform complex conditional logic into readable formats.

```
DATA(greeting) = VALUE string( |Hello, world!| ).
```

```
DATA(target_row) = CORRESPONDING ty_s_target( source_row MAPPING id = src_id title = name ).
```

```
DATA(message) = COND string( WHEN sy-subrc = 0 THEN 'Operation successful' ELSE 'Operation failed' ).
```

```
DATA(rv_text) = SWITCH string( iv_cat
						WHEN 'A' THEN 'Pome fruit'
						WHEN 'B' THEN 'Tropical fruit'
						WHEN 'C' THEN 'Stone fruit'
						ELSE 'Unknown' ).
```


Using those features does not spare you to be performance aware. Continue to choose the table type for your internal tables wisely despite using table expressions as table expressions as such do not provide better performance compared to looping or reading the internal table. 

### Further reading

#Article [Cheat Sheet Modern ABAP](https://www.brandeis.de/en/blog/cheat-sheet-modern-abap-en)