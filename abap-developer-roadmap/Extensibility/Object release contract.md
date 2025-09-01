#Basic 

The API state of SAP ABAP repository objects and their release contract play a role in supporting the tiered ABAP extensibility model, which distinguishes between classic extensibility using the **ABAP Standard** language version and developer extensibility utilizing the **ABAP for Cloud Development** language version. The API state is a gateway for these extensibility models, determining the accessibility and modifiability of ABAP repository objects. 

In **classic extensibility** developers can leverage the complete spectrum of ABAP capabilities, extending and using all ABAP repository objects irrespective of their API state to tailor SAP applications directly within the system. It is up to the developers to uphold a healthy balance between flexibility of customization and core system integrity. Classic extensibility is available in the On Premise and Private Cloud Edition ABAP Environment only. 

Conversely, in **developer extensibility** the API state identifies which objects can be extended or used as it allows to extend or use released ABAP repository objects only. Developer extensibility thus focuses on creating upgrade stable extensions, prioritizing clean core principles and integration with SAP cloud solutions. In the BTP ABAP Environment developer extensibility is enforced.

Hint: in the 'Open ABAP Development Object' Dialog (ctrl + shif + a) try using e.g. 'type:ddls api:use_in_cloud_development i_sales' to find all released CDS views in the area of Application Component Sales and Distribution.
## Further reading

#Article [Three tier extensibility model](https://learning.sap.com/learning-journeys/practicing-clean-core-extensibility-for-sap-s-4hana-cloud/explaining-extensibility-model-best-practices_e290f382-800e-40ef-a203-85a13115f487)
#Article [Finding Released Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/3f232ac7cecc4d9891ff512462240223.html?locale=en-US)


