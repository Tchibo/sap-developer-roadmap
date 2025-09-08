> [!todo] Behaviour definition scope
> - [ ] Other than 'permitted operations' do mention operations including validation, determinations, authorization control, feature control, draft handling etc. 
> 	- [ ] Explained in BDL.

Core Data Services (CDS) view entities provide only read access to data. To enable transactional capabilities, CDS entities are combined with two additional file types. A complete RAP entity consists of three development objects:

1. The **CDS entity** defines the field list, relationships to other views, and entity type (root or child).
2. The **behavior definition** specifies the behavior provided for the entity.
3. The **behavior implementation** contains the actual behavior logic through an ABAP behavior pool with local classes specific to the RAP business object.

## Resources
- [RAP BO Behavior](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/169c5ada6c1543eba44d0aa27d7f0578.html?locale=en-US)
- [SAP Help Portal | Introduction to EML](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/af7782de6b9140e29a24eae607bf4138.html?locale=en-US&q=facet)
- [Draft Handling](https://help.sap.com/docs/ABAP_PLATFORM_NEW/fc4c71aa50014fd1b43721701471913d/a81081f76c904b878443bcdaf7a4eb10.html?locale=en-US)