---
tags:
  - cap-cds
  - basic
links:
  - "[[Domain Modelling]]"
source: https://cap.cloud.sap/docs/guides/domain-modeling#namespaces
aliases:
  - cds-namespace
  - CDS Namespace
---
You can use [namespaces](https://cap.cloud.sap/docs/cds/cdl#namespaces) to get to unique names without bloating your code with fully qualified names. For example:

```cds
namespace foo.bar;
entity Boo {}
entity Moo : Boo {}
```

...is equivalent to:

```
entity foo.bar.Boo {}
entity foo.bar.Moo : foo.bar.Boo {}
```

**Note**:
- **Namespaces are just prefixes** — which are automatically applied to all relevant names in a file. Beyond this there's nothing special about them.
- **Namespaces are optional** — use namespaces if your models might be reused in other projects; otherwise, you can go without namespaces.
- The **reverse domain name** approach works well for choosing namespaces.

**Sources**
- [SAP Capire - Namespaces](You can use [namespaces](https://cap.cloud.sap/docs/cds/cdl#namespaces) to get to unique names without bloating your code with fully qualified names. For example:)