#Basic 
Clean ABAP is a practical guide that strengthens readability, simplicity, and testability, leading to consistent standards, easier maintenance, faster reviews, and fewer defects. As a result, solutions become more stable and upgrade-ready (e.g., towards S/4HANA, RAP), and teams work more efficiently together. At the same time, Clean ABAP isn’t dogma: in some cases, teams deliberately deviate from the rules to meet business directives, regulatory requirements, or hard constraints. It’s important to justify such deviations transparently and actively manage the associated risks.

Clean ABAP is a voluntary, community-driven style and design guide at the code level (readability, testability, naming, small methods, exceptions instead of SY-SUBRC). SAP guidelines are product- and release-bound, partly mandatory rules at the architecture and compliance level (Clean Core, extensibility/RAP, security, performance, released APIs).

# Examples 

Prefer CASE over ELSEIF for multiple mutually exclusive alternatives because it improves clarity and readability.

Example:
```abap
CASE type.
  WHEN type-some_type.
    " ...
  WHEN type-some_other_type.
    " ...
  WHEN OTHERS.
    RAISE EXCEPTION NEW /clean/unknown_type_failure( ).
ENDCASE.
```

Anti-pattern:
```abap
IF type = type-some_type.
  " ...
ELSEIF type = type-some_other_type.
  " ...
ELSE.
  RAISE EXCEPTION NEW /dirty/unknown_type_failure( ).
ENDIF.
```


Use methods instead of comment blocks to structure code into meaningful steps; this clarifies intent, structure, and dependencies and avoids carry-over errors.

Example:
```abap
DATA(statement) = build_statement( ).
DATA(data)      = execute_statement( statement ).
```

Anti-pattern:
```abap
" -----------------
" Build statement
" -----------------
DATA statement TYPE string.
statement = |SELECT * FROM d_document_roots|.
" -----------------
" Execute statement
" -----------------
DATA(result_set) = adbc->execute_sql_query( statement ).
result_set->next_package( IMPORTING data = data ).
```

# Resources

#website [Clean ABAP](https://github.com/SAP/styleguides/blob/main/clean-abap/CleanABAP.md)
#course  [The Golden Rules](https://github.com/SAP/styleguides/blob/main/clean-abap/cheat-sheet/CleanABAPTheGoldenRulesV1.1.1.pdf)
#course  [Clean ABAP Cheat Sheet](https://github.com/SAP/styleguides/blob/main/clean-abap/cheat-sheet/CleanABAPCheatSheetV1.4.1.pdf)

