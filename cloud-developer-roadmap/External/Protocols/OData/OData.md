---
tags:
  - odata
  - protocols
links:
source: https://aichat.tchibo.ai/s/8dcda536-eaa1-42ef-9371-9ce51edc2263
---
> [!toDo] Tchibo preference is V4
> Do mention that new apps are to be created with the V4 Protocol version only.

[OData]] (Open Data Protocol) is a standardised protocol for data exchange developed by [[Microsoft]]. It enables:
- Standardised access** to data via HTTP/HTTPS
- queries** with URL-based language
- **Manipulation of data** (create, update, delete)
- Standardised formats** ([[JSON]], [[XML]])

> For [[Tchibo]], [[OData]] offers an efficient connection of data sources to applications, especially in the [[SAP]] environment, e.g. for [[SAP Fiori]] and [[API]] services.

**Differences between [[OData v2]] and [[OData v4]]**

**[[OData v2]]**
- Older standard, widely used in [[SAP]] systems
- [[XML]] as standard, [[JSON]] optional
- Simpler data model
- More limited query options and metadata

**OData v4]]**
- Modern standard with extended functions
- [[JSON]] as standard format
- Improved performance and queries (filters, aggregation, navigation)
- Support for actions, functions, batch processing
- Better authorisation and security support

> In the [[Tchibo]] context, many existing [[SAP Fiori]] apps and older [[SAP]] systems use V2, while new [[SAP S/4HANA]] solutions are increasingly using V4.