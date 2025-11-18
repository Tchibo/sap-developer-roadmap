#Basic 

Developer extensibility in the On Premise and BTP ABAP Environment empowers ABAP developers using Eclipse ABAP Development Tools (ADT) to create custom enhancements and extensions that surpass the options available with key user extensibility. 

While for Side-by-side Extensibility extensions should be based on **'ABAP Cloud Development'** preferably, for on-stack extensibility in on Prem or Private Cloud systems also **'Classic ABAP Development'** can be used.
### Extensions with ABAP Cloud Development 
Here Developer Extensibility uses **ABAP language version 'ABAP for Cloud Development'** and hence only SAP Standard or custom objects with a 'release contract' may be used. Within the Clean Core Extensibility Model this corresponds to Level A Extensions.

This leads to extensions that are: 
- **Cloud-Ready:** Designed for cloud environments, ensuring upgrade stability. 
- **Upgrade Stable:** Extensions are designed to be compatible with future system upgrades. 
- **Released APIs:** Relies on released APIs and extension points provided by SAP. 
- **ABAP Cloud:** Utilizes the ABAP Cloud development model for custom development. 
### Extensions with Classic ABAP Development
Here Developer Extensibility uses **Standard ABAP language** and enables therefore the use of objects for extensions that don't have an object stability contract. Still as clean core seen are objects within level B that are basically classic API's and approved development patterns (see for details Clean Core Extensibility Model).
## Further Reading

#Article [Extend SAP S/4HANA in the cloud and on premise with ABAP based extensions](https://www.sap.com/documents/2022/10/52e0cd9b-497e-0010-bca6-c68f7e60039b.html)
#Article [ABAP Language Versions](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_versions.htm)
### Resources
#website [Cloudification Repository Viewer](https://sap.github.io/abap-atc-cr-cv-s4hc/?states=noAPI)


