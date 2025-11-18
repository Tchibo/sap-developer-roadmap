#Basic 

As entirely clean core defined is the usage of Level A interfaces for extensions in the Clean Core Extensibility Model. These objects come with a **stability contract** that ensures the stability of the interfaces.  

There are three categories of release contracts:
- C0 - Extensibility
- C1 - Use System Internally 
- C2 - Use as a remote API

While C0 means that the interface can be extended itself, C1 and C2 defines if it can be used within the system for on-stack Extensibility (C1) or for side-by-side Extension (C2).

Hint: in the 'Open ABAP Development Object' Dialog (ctrl + shif + a) try using e.g. 'type:ddls api:use_in_cloud_development i_sales' to find all released CDS views in the area of Application Component Sales and Distribution.
## Further reading
#Article [Finding Released Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/3f232ac7cecc4d9891ff512462240223.html?locale=en-US)


