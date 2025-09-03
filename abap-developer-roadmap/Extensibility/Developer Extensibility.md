#Basic 

Developer extensibility in the On Premise and BTP ABAP Environment empowers ABAP developers using Eclipse ABAP Development Tools (ADT) to create custom enhancements and extensions that surpass the options available with key user extensibility. Developer Extensibility by definition uses **ABAP language version 'ABAP for Cloud Development'** and hence only SAP Standard or custom objects with a 'release contract' may be used. This leads to extensions that are: 

- **Cloud-Ready:** Designed for cloud environments, ensuring upgrade stability. 
- **Upgrade Stable:** Extensions are designed to be compatible with future system upgrades. 
- **Released APIs:** Relies on released APIs and extension points provided by SAP. 
- **ABAP Cloud:** Utilizes the ABAP Cloud development model for custom development. 

Whether developer extensibility is enforced or classic extensibility is allowed in the On Premise ABAP Environment depends on the ABAP language version set on the affected repository object. The ABAP language version is defaulted from the ABAP package containing the object. In the BTP ABAP Environment classic extensibility is not available, as the ABAP language version 'ABAP for Cloud Development' is enforced.

SAP speaks of a 3 tier extensibility model for ABAP developers. In tier 1 language version 'ABAP for Cloud Development' is used with released SAP Standard objects only (developer extensibility). In tier 2 with language version 'Standard ABAP' additionally non-released SAP Standard objects are wrapped and released for use in custom development. In tier 3 with language version 'Standard ABAP' additionally non-released objects are used directly (classic developer extensibility).

## Further Reading

#Article [Extend SAP S/4HANA in the cloud and on premise with ABAP based extensions](https://www.sap.com/documents/2022/10/52e0cd9b-497e-0010-bca6-c68f7e60039b.html)
#Article [Explaining Developer Extensibility](https://learning.sap.com/learning-journeys/practicing-clean-core-extensibility-for-sap-s-4hana-cloud/explaining-developer-extensibility_f2683861-d69e-4a59-9e3e-01e3cc20fb0f)
#Article [ABAP Language Versions](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abenabap_versions.htm)

