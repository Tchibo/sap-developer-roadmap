#Basic 

Object-oriented programming (OO) was added to the ABAP language in the late 1990s and has been the preferred approach since.  
It improves readability, maintainability, testability, and robustness. Code is split into small, focused units, bundling data and behavior into objects. OO promotes separation of concerns, reusability, and modularity via inheritance and polymorphism. Exception classes enable structured error handling and diagnostics, replacing earlier return codes. AMDP enables methods in HANA SQLScript that run on the database (code pushdown).

Classic ABAP structures code around subroutines, includes, and function pools, with data moving freely between them. ABAP Unit is class-based, so tests target classes; procedural code cannot be tested directly and usually needs OO wrappers. OO also improves control over variable visibility and lifetime; in procedural ABAP, globals were common and often unavoidable. SAP has marked many elements obsolete—most notably header-line tables—creating interoperability issues when mixed with procedural ABAP.

Until recently, ABAP Objects often sat behind a thin procedural entry point (e.g., an executable report) delegating to classes. In modern releases, SAP has reduced the need for such entry points through non-procedural channels like RAP-based services, Fiori apps, and Application Jobs. This shift benefits both ABAP Cloud and standard ABAP.
### Resources
- #Article [ABAP Objects as a Programming Model](https://help.sap.com/doc/abapdocu_752_index_htm/7.52/en-US/abenabap_obj_progr_model_guidl.htm)
- #Video [Object-Oriented Programming, Simplified](https://www.youtube.com/watch?v=pTB0EiLXUC8)