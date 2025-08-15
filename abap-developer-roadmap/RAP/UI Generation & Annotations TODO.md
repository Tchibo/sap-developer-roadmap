#Medium 
- [ ] #todo #edna  rework, join parts
In RAP, the UI is generated based on **CDS UI annotations** in the CDS entities. Annotations can either target a single field (e.g. adding a label or adding a value help) or they can influence a whole entity (e.g. creating a UI field group called 'facet' or enabling free text search).
##### RAP UI Elements
These are the functionalities that shape the UI of a RAP application:
- **Facets** are UI elements like lists or field groups that define the layout of a RAP application.
- **Selection fields** are filters on a list view.
- **Value helps** are a key factor to make applications resilient and user friendly. **Additional bindings** can be used to bind a value help to another field enabling auto-completion and filtering.

``` cds
@UI.headerInfo.title.value: 'CustomerName'
@Search.searchable: true
define view entity C_Customer
	as select from kna1
{
@UI.facet: [ {
		label: 'Customer Details',
		type: #FIELDGROUP_REFERENCE,
		targetQualifier: 'customer_details'
} ]

	@Search.defaultSearchElement: true
key CustomerId,

	@EndUserText.label: 'Customer Name'
	@UI.fieldGroup: [ { qualifier: 'customer_details' }]
	@Search.defaultSearchElement: true
	CustomerName
}
```



## Resources
- [SAP Help Portal | Develop UI-Specifics](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/024de050bbe544498d425d48106141e6.html?locale=en-US)
- [SAP Help Portal | List of all CDS Annotations](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/130e02a697e14bf8b05dd6672c56250b.html?locale=en-US)
- [Selection Fields](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/e27b082ff3b849d8adba927794ffbd4f.html?locale=en-US&q=feature+control)


#Medium
RAP also provides a bunch of more sophisticated UI features. Some of them are:  

- 
- **Selection** and **presentation variants** allow to add additional filters or modify the way data is presented in a certain facet.
- **Charts** and **data points** enable to visualize data.
- **Navigation** can be used to navigate to different applications or web sites.

## Resources
- [Visualizing Data with Charts](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/c7f12219d533404f8fad96aa68fa4ba6.html?locale=en-US&q=feature+control)
- [Field Manipulation, Data Points and Navigation](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/269ce7a318b44b21b048c0e966479c9c.html?locale=en-US&q=feature+control)
- [SAP RAP Showcase App - Presentation and Selection Variants](https://github.com/SAP-samples/abap-platform-fiori-feature-showcase/blob/main/06_object_page_content.md#presentation-variant---object-page)