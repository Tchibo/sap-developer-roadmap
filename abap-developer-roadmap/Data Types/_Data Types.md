ABAP is a statically typed language, requiring variables to be typed before use to ensure data consistency, efficient memory usage, and minimize runtime errors.

Traditional ABAP provides two tools for creating data types: the **ABAP Dictionary** and ABAP TYPE definitions. ABAP Dictionary types are defined in a global repository and shared among programs, while TYPE definitions are created directly in ABAP code using the **`TYPE` keyword**. A newer option, **CDS entity types**, will be discussed separately in the CDS chapter.

Both ABAP Dictionary types and TYPE definitions are crucial in modern ABAP coding, each with advantages and disadvantages. Dictionary types offer a central, reusable definition beneficial for frequently used types. They contain additional metadata, such as text labels for end users, fixed domain values, and conversion exits. Database tables must be created via the ABAP Dictionary.

In contrast, TYPE definitions, bound directly to source code, are more flexible and simpler for numerous or less reusable types. They also allow inline documentation but cannot be reused in the Dictionary or CDS entities.

## When to use which?  
Typically, ABAP Dictionary types suit frequently reused elementary data types, while TYPE definitions are better for structures and table types.
### Resources

