---
tags:
  - cap-cds
  - cds
  - cdl
  - basic
links:
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/cds/common#common-reuse-aspects
aliases:
  - aspect
  - aspects
  - Aspects
---
> [!todo] The meaning of 'map entity structures' needs clarification or rewording
> Even to the initiated reader 'map entity structure' does not seem to clearly outline the benefit of using 'aspects' in domain data modeling. To me an 'aspect' defines the attributes that go with specific context, e.g. 'key definition', 'amount definition', 'text definition' etc. and as such can be reused by entities in such contexts.

Aspects can be used to map entity structures, which can then be inherited when defining a new entity. [[SAP]] already provides some frequently used aspects under the namespace `sap.common`, which can be "implemented" in the data model.

**Example
```cds
aspect CustomValueHelp {
	name : localised String(80);
	description : localised String(250);
}

entity BusinessPartnerVH : CustomValueHelp {
	key bupa : String(80);
}

// Is equivalent to
entity BusinessPartnerVH {
	key bupa : String(80);
		name : localised String(80);
		description : localised String(250);
}
```

Existing entities can also be extended by an [[Aspect]].

**Example
```
aspect ProductInformation {
	category: Association to one ProductCategory;
	name: localised String;
	description: localised String;
}

entity ToyCar {
	colour: String;
}

extend ToyCar with ProductInformation;

// Is equaivalent to
entity ToyCar : ProductInformation {
	colour: String;
}
```

> [!TIP]
> The extension of entities is particularly helpful/useful if existing aspects or entities from a "foreign" data model or from a [[CDS plugin]] must/should be extended.

**Sources**
- https://cap.cloud.sap/docs/cds/common#common-reuse-aspects
- https://cap.cloud.sap/docs/cds/aspects
- [SAP Capire - Entites & Type Definitions](https://cap.cloud.sap/docs/cds/csn#type-definitions)