#Basic 

Exception classes enable structured error handling. They behave like normal classes but are handled with ABAP constructs such as `TRY...CATCH...ENDTRY` and `RAISE EXCEPTION`.

Exception classes can define special `CONSTANTS` that link to a message class (text IDs). A message can be attached via `MESSAGE ... RAISING` or by reusing the last message with `RAISE EXCEPTION ... USING MESSAGE`.

## Static vs. Dynamic Check

Every exception class inherits from `cx_static_check` or `cx_dynamic_check`. A method that raises a **static** exception must either handle it locally or declare it in its signature; otherwise the code check reports a warning. Use static exceptions for conditions you can foresee and handle.

**Dynamic** exceptions are for unexpected edge cases that usually aren’t handled and can lead to a runtime error—for example, a client disconnect during processing. They don’t need to appear in method signatures, but you can still catch them with `TRY...CATCH`. When accessing an internal table by a non-existent index, the dynamic exception `cx_sy_itab_line_not_found` is raised.

# Resources
#website [Exception Classes](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/abenexceptions_classes.html)
#course [Working with Exception Classes](https://learning.sap.com/learning-journeys/acquire-core-abap-skills/working-with-exception-classes_acd9568c-be4e-445a-a454-14c6f2cfcd2e)