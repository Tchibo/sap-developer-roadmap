#Basic 

> [!toDo] Method parameters typed with reference to interface
> ...perhaps deserve a special mention as it gives the method implementation a handle to deal with object instances that are not related by inheritance.

In ABAP, an **interface** defines **method signatures**, **constants** and **types** without providing an implementation. It acts as a contract: any class that implements the interface must provide concrete implementations for all defined methods. Unlike inheritance, interfaces do not dictate structure or behavior beyond what is declared, which allows developers to combine multiple interfaces in one class. Interfaces allow a calling method to call a set of different classes in the same way, as they all share the same method signature through their interface. 

For testability it is best to always start with the interface definition before creating a class. Variables can by typed to interfaces and it is good practice to do so.

While Interfaces support **constants and types**, it is best practice *not* to define types in Interfaces if they are re-used between classes and instead opt for either an abstract class or a definition in the ABAP Dictionary.

Interfaces play an important role in **BAdIs**: SAP delivers the interface definition, while customers implement it according to their needs. This ensures extensibility without modifying standard code.

In RAP, Interfaces are not used - *local handler* and *saver* classes are subclasses and type definitions are handled by additions to the ABAP language ("``TYPE FOR...``").

# Resources
#course [Defining Interfaces](https://learning.sap.com/learning-journeys/acquire-core-abap-skills/defining-interfaces_ab3c7c07-bb66-424b-ba06-6cfa7cc39439)
#article [Understanding polymorphism](https://community.sap.com/t5/application-development-and-automation-blog-posts/understanding-polymorphism/ba-p/13447968)
