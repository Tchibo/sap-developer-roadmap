#Basic 

ABAP implements many object-oriented principles familiar from other languages:

- Classes are instantiated by their **constructor**.
- Methods and variables can be **public, protected, or private**.
- A subclass **inherits** methods and variables from its superclass; inherited methods may be **redefined**.
- **Abstract classes** cannot be instantiated.
- Classes can be **friends**, allowing access to a friend’s protected items.
- **Local classes** are usable only within their creation context.
- **Interfaces** define method signatures without implementation; a class can implement several. With subclasses, they are often used in BAdIs: SAP delivers the signature, the customer the implementation.
# ABAP specifics
## Dictionary
Most types are defined in the Dictionary for reuse across the system. Public types in ABAP classes can also be reused, often for derived types.
## Variables are not objects
Variables are never objects, but references and field symbols can point to them.
## Global Classes
A **global class** consists of several repository objects:

1. The **global class**, instantiated from other classes or programs.
2. **Class-relevant local types**, visible only within the global class. Deferred local classes are declared here and implemented in _Local types_.
3. **Local types**, implementing local classes.
4. **Test classes** for ABAP Unit tests.
5. The **macro**, a legacy artifact rarely used today.
 
# Resources
#article [Working with ABAP Classes](https://help.sap.com/docs/ABAP_PLATFORM_BW4HANA/c238d694b825421f940829321ffa326a/1fbf9bd2d6664b88982173af52765a03.html?locale=en-US&q=Class+pool)
#course [Working with Local Classes](https://learning.sap.com/learning-journeys/acquire-core-abap-skills/defining-a-local-class_d4f46591-157b-468f-b94a-8d484d5ddca9)
