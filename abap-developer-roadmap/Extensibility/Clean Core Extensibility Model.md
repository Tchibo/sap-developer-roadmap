#Basic
In the new model extensions are labeled regarding their clean core rating reaching. In this model Level A and Level B ratings are considered clean core.
### Level  A
Extensions qualify for Level A when they are built solely on **publicly** **released** SAP APIs and extension points. Publicly released Objects are officially supported, documented and governed under a clearly defined stability contract by SAP. (see also Object stability contract)
### Level B
Customer extensions qualify for Level B when they use only SAP objects and development patterns officially classified as classic APIs or released APIs.
### Level C
Contains SAP internal objects that are not classified nor intended for customer use - but still are used. By default **all** SAP objects are considered internal when they are **not** designated as **released** (Level A), nominated as **classic APIs** (Level B) nor explicitly classified as **not recommended** (Level D).
### Level D
Includes all objects and patterns that have been officially declared as not recommended for external use. This includes objects labeled with the “noAPI” designation in Cloudification Repository as well as all development patterns that are not considered to be clean core.

### Resources
#Article  [Cloudification Repository Viewer](https://sap.github.io/abap-atc-cr-cv-s4hc/?states=classicAPI)
#Article [3578329 - Frameworks, Technologies and Development Patterns in Context of Clean Core Extensibility - SAP for Me](https://me.sap.com/notes/3578329)
#Article [Clean Core Extensibility Whitepaper](https://d.dam.sap.com/a/juG2xVj/99719_White%20paper_96262.pdf?rc=10&inline=true)