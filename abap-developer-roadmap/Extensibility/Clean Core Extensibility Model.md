#Basic
In the new model, extensions are labeled according to their Clean Core compliance level. In this model, Level A and Level B are considered clean core.
### Level A
Extensions qualify for Level A when they are built solely on **publicly released** SAP APIs and extension points. Publicly released objects are officially supported, documented, and governed by SAP under a clearly defined object stability contract (see also Object Stability Contract).
### Level B
Customer extensions qualify for Level B when they exclusively use SAP objects and development patterns officially classified as **released APIs** or **classic APIs**.
### Level C
Level C is assigned when extensions use SAP internal objects that are neither classified for customer use nor intended as released or classic APIs. **All** SAP objects are considered internal by default **unless** they are designated as **released** (Level A), nominated as **classic APIs** (Level B), or explicitly classified as **not recommended** (Level D).
### Level D
Includes all objects and development patterns that have been explicitly declared as **not recommended** for external use. This includes objects labeled with the *noAPI* designation in the Cloudification Repository, as well as development patterns that are not considered clean core.

### Resources
#Article  [Cloudification Repository Viewer](https://sap.github.io/abap-atc-cr-cv-s4hc/?states=classicAPI)
#Article [3578329 - Frameworks, Technologies and Development Patterns in Context of Clean Core Extensibility - SAP for Me](https://me.sap.com/notes/3578329)
#Article [Clean Core Extensibility Whitepaper](https://d.dam.sap.com/a/juG2xVj/99719_White%20paper_96262.pdf?rc=10&inline=true)