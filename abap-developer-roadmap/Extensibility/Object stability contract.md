#Basic 

In the Clean Core Extensibility Model, the exclusive use of Level A interfaces for extensions is considered fully clean core. These objects are provided with a **stability contract** that ensures long-term interface stability.

Several release contracts are available:
- **C0** - Extensibility
- **C1** - Use system-internally
- **C2** - Use as a remote API
- **C3** - Manage configuration content
- **C4** - Use in ABAP-Managed Database Procedure

While **C0** indicates that an interface itself may be extended, **C1**, **C2** and **C4** define how an interface can be consumed: either within the system for on-stack extensibility (**C1** and **C4**) or externally for side-by-side extensibility (**C2**). **C3** allows developers to manage their own configuration content.

**Hint:** In the *Open ABAP Development Object* dialog (Ctrl + ⇧ + A on Windows, ⌘ + ⇧ + A on Mac), you can use search filters such as `type:ddls api:use_in_cloud_development i_sales` to find all released CDS views in the Sales and Distribution application component.

## Further reading
#Article [Finding Released Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/3f232ac7cecc4d9891ff512462240223.html?locale=en-US)
#Article [Released APIs](https://help.sap.com/docs/ABAP_PLATFORM_NEW/c238d694b825421f940829321ffa326a/c479660d07374c15a1a5fe83fdbb1337.html?locale=en-US)


