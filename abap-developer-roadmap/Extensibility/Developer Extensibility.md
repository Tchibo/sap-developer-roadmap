#Basic 

Developer extensibility, both on-premise and in BTP ABAP Environment, empowers ABAP developers using Eclipse ABAP Development Tools (ADT) to create custom enhancements and extensions that go beyond the options available with key user extensibility. 

While side-by-side extensions are preferably based on **ABAP for Cloud Development**, **Classic ABAP Development** can also be used for on-stack extensibility in on-premise and private cloud systems.
### Extensions with ABAP Cloud Development
Here, developer extensibility uses **ABAP language version 'ABAP for Cloud Development'**. Therefore, only SAP Standard or custom objects with a release contract may be used. Within the Clean Core Extensibility Model, this corresponds to Level A extensions.

This leads to extensions that are: 
- **Cloud-Ready:** Designed for cloud environments, ensuring upgrade stability. 
- **Upgrade Stable:** Extensions are designed to be compatible with future system upgrades. 
- **Released APIs:** Relies on released APIs and extension points provided by SAP. 
- **ABAP Cloud:** Utilizes the ABAP Cloud development model for custom development. 
### Extensions with Classic ABAP Development
Here, developer extensibility uses the **standard ABAP** language version. Therefore, extensions may use objects that do not have an object stability contract. From a Clean Core perspective, objects classified as Level B are still considered compliant, as they essentially represent classic APIs and approved development patterns (see the Clean Core Extensibility Model for details).

## Further Reading
#Article [Extend SAP S/4HANA in the cloud and on premise with ABAP based extensions](https://www.sap.com/documents/2022/10/52e0cd9b-497e-0010-bca6-c68f7e60039b.html)
#Article [ABAP Language Versions](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_versions.htm)
### Resources
#website [Cloudification Repository Viewer](https://sap.github.io/abap-atc-cr-cv-s4hc/?states=noAPI)


