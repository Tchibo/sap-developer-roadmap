#Advanced 

Using Fiori Tools in SAP Business Application Studio you can a.) extend custom built Fiori Elements applications or b.) use the UI5 Adaptation Editor to extend SAP Standard Free Style and Fiori Elements apps under the condition that the original app uses asynchronous views only. The result of using Fiori Tools are 'Controller Extensions' that allow you to add or hide fragments, add custom UI logic or override standard Fiori Elements behaviour.

Using Controller Extensions you can a.) add custom event handler methods and/or b.) change standard behaviour of Fiori Elements (by defining 'overrides' for overrideable features and their lifecycle hooks). Using a 'routing' override for lifecycle hook 'onBeforeNavigation' you can e.g. change the object page that the Fiori Elements List Report page navigates to on line item click.

Controller Extensions of a Fiori Elements application are governed by the 'Flexible progamming model' (FPM). The FPM describes the extension points to add custom fragments, the building blocks you can use to provide content and the controller extensions to implement custom logic. In addition to FPM building blocks you can use any UI Control provided with SAPUI5.

## Further reading

#Article [Adapt the UI using UI5 Adaptation Projects](https://help.sap.com/docs/bas/developing-sap-fiori-app-in-sap-business-application-studio/adapt-ui)
#Article [Create an extension controller in UI5 Adaptation Project](https://help.sap.com/docs/bas/developing-sap-fiori-app-in-sap-business-application-studio/adapt-ui)
#Article [Overrideable Fiori Elements Features](https://help.sap.com/docs/bas/developing-sap-fiori-app-in-sap-business-application-studio/adapt-ui)
#Article [Flexible Programming Model](https://ui5.sap.com/test-resources/sap/fe/core/fpmExplorer/index.html#/overview/introduction)
#Article [UI5 Demokit](https://ui5.sap.com/)



