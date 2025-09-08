> [!todo] Rather just mention under UI Annotations?
> Facets as one of the @UI annotations seems to get too much attention compared to the others by making it a separate article. Perhaps just mention under 'UI Annotations'

Facets are building blocks on the object page of a RAP UI. They can appear in the header or in the body section. They can be field groups, lists of entries (line items), charts, or collections that group other facets.
```
@UI.facet: [ {
		label: 'Customer Details',
		type: #FIELDGROUP_REFERENCE,
		targetQualifier: 'customer_details'
	} ]
```
#### Commonly used properties
- `label`: Adds a headline to the facet.
- `type`: Specifies the facet kind (field group, chart, line item, collection).
- `position`: Controls the display order of facets.
- `targetQualifier`: Marks which fields belong to the facet via a shared qualifier.
- `targetElement`: Points to an association where the facet’s fields are defined. If they are not part of the current entity.
- `id`: Ids are mainly used in collections to be referenced by sub-facets via `parentId`.
#### Resources
- #website [Grouping Fields | SAP Help Portal](https://help.sap.com/docs/abap-cloud/abap-rap/grouping-fields?locale=en-US)