#Advanced 

Standard Fiori Apps that use synchronous views or do not use stable IDs for their UI controls can only be extended using 'Component Configuration'. Component configuration is done in Fiori **extension projects**. If and when required you are advised to create an extension project (instead of an adaptation project) while using the 'SAP UI5 Adaptation Project' application generator template.

In the process of extending the original application component configuration entries are added to its manifest.json. The type of manifest configuration entry that gets added depends on the type of extension you choose in 'Create extension' (on 'right click' of file .extconfig.json). You have the option to a.) extend a view controller, b.) extend a view, c.) hide a control on a view or to d.) replace a view. 

To replace a button on a view and navigate to another app on press for example you would hide the original button (hide a control), add a fragment to the view to hold the new button (view extension) and implement an button 'Press' event handler to perfrom cross-app navigation (controller extension).

An app extension must run alongside its related original SAP standard app. Use the Fiori command 'Fiori: Add Deployment Configuration' and then 'Fiori: Deploy Application' to deploy the extension to the ABAP Platform where the original application is running.

## Further reading

#Article [Using component configuration](https://ui5.sap.com/#/topic/c264d66d6e3c4104818bc52c174a000c)
