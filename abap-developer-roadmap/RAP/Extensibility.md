RAP extensibility allows creating lifecycle-stable extensions for RAP business objects (BO). Extensibility is used when a BO should not be modified (like **SAP standard BO**s) or when extension logic should remain separate (for temporary or specialized use cases).

RAP BOs can be extended in terms of their data model and behavior. Extensions can be done on each level (database persistence, interface entity, projection, service definition).

**Node extensibility** is a special extension type. It adds a new BO entity to an existing RAP BO. The extension BO becomes a child of the original BO. It maintains its own persistence, data model, and behavior while being managed by the extended root BO.

Development objects must be **enabled for extension** using the keyword `extensible` or the annotation `@AbapCatalog.extensibility`.
## Resources
- #website [Extend | SAP Help Portal](https://help.sap.com/docs/abap-cloud/abap-rap/extend?locale=en-US)
