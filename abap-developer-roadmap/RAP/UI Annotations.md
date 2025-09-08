A RAP-based Fiori UI usually consists of a list page (that contains a filter bar and a list of entries) and one or more object pages, that show the details of certain data entity.
In RAP, the **Fiori Elements** UI is generated based on **CDS UI annotations** in the CDS entities. Annotations are typically defined in the metadata extension of a projection view. 
Annotations can either target a single field (e.g. adding a label or adding a value help) or they can influence a whole entity (e.g. creating a UI field group or enabling free text search).

 The most vital annotations, that shape the UI of a RAP application are the following:
- **Line items** define a list of entries.
- **Selection fields** are filters on a list page.
- **Facets** are UI elements like lists or field groups that define the layout of an object page.
- **Value helps** provide a list of valid entries and are a key factor to make applications resilient and user friendly. 

``` cds
@UI.headerInfo.title.value: 'CustomerName'
@Search.searchable: true
define view entity C_Customer as select from I_Customer {

	@UI.facet: [ {
		label: 'Customer Details',
		type: #FIELDGROUP_REFERENCE,
		targetQualifier: 'customer_details'
	} ]
	
	@EndUserText.label: 'Customer Name'
	@UI.fieldGroup: [ { qualifier: 'customer_details', position: 20 }]
	@Search.defaultSearchElement: true
key	CustomerId,
	...
}
```

## Resources
- #website [SAP Help Portal | Develop UI-Specifics](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/024de050bbe544498d425d48106141e6.html?locale=en-US)
- #website [SAP Help Portal | List of all CDS Annotations](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/130e02a697e14bf8b05dd6672c56250b.html?locale=en-US)
- #website [Selection Fields](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/e27b082ff3b849d8adba927794ffbd4f.html?locale=en-US&q=feature+control)
- #website [Grouping Fields | SAP Help Portal](https://help.sap.com/docs/abap-cloud/abap-rap/grouping-fields?locale=en-US)