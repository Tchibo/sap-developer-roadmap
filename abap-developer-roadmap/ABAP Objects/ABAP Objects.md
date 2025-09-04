#Basic 

> [!todo] More detail about key qualifying attributes of OO compared to legacy?
> Als Idee: ABAP Object-Oriented (ABAP OO) differs from procedural ABAP by ==bundling data and functions into objects, promoting code reusability and modularity through inheritance and polymorphism==. Procedural ABAP, the older style, structures programs around procedures, function modules, and subroutines, with data able to move freely between functions. 

Object-oriented programming (OO) was added to the ABAP language in the late 1990s and has been the preferred approach for new code since then.
It improves readability, maintainability, testability, and robustness. Code is split into smaller, more focused units than are usually found in classic procedural ABAP. Separation of concerns and clearly structured interfaces enable code reuse, and onboarding new developers is faster. ABAP Unit is class-based, so automated tests are written against classes; procedural code cannot be unit-tested directly and typically needs OO wrappers.
It also gives better control over variable visibility and lifetime; in procedural ABAP, global variables were common and sometimes unavoidable. SAP has marked many language elements as obsolete - most notably header-line tables - which often causes interoperability issues when mixing with procedural ABAP.

Until recently, ABAP Objects was often used behind a thin procedural entry point (for example, an executable report) that delegated to classes. In recent releases, SAP has been reducing the need for procedural entry points through modern, non-procedural entry channels such as RAP-based services, Fiori apps, and Application Jobs. This shift benefits both ABAP Cloud and Standard ABAP.

> [!toDo] Special mention of exception classes 
> You might want to dedicate exception classes a separate subtopic as they fundamentally introduced proper error handling instead of just return code handling in modularized code.

> [!toDo] Special mention of classes responsible for AMDP 
> You might want to dedicate classes that implement AMDP a separate subtopic as they gave us the power of code pushdown. Also in respect of table function entities in CDS, that make use of AMDP for code push-down.

### Resources
- #Article [ABAP Objects as a Programming Model](https://help.sap.com/doc/abapdocu_752_index_htm/7.52/en-US/abenabap_obj_progr_model_guidl.htm)
- #Video [Object-Oriented Programming, Simplified](https://www.youtube.com/watch?v=pTB0EiLXUC8)