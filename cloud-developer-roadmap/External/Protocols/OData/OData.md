---
tags:
  - odata
  - protocols
links:
source: https://aichat.tchibo.ai/s/8dcda536-eaa1-42ef-9371-9ce51edc2263
aliases:
  - Open Data Protocol
---
OData (Open Data Protocol) is a standardised protocol for data exchange developed by [[Microsoft]]. It enables uniform access to data via [[HTTP]] or [[HTTPS]], supports queries through a URL-based language, allows manipulation of data such as creating, updating, or deleting records, and uses standardised formats like [[JSON]] and [[XML]].

For Tchibo, OData offers an efficient way to connect data sources to applications within the [[SAP]] landscape, particularly in scenarios involving [[SAP Fiori]] apps and [[API]] services.

**Differences between OData V2 and OData V4**

[[OData V2]] represents the older standard that is still widely used in [[SAP]] systems. Its default format is [[XML]], while [[JSON]] is only optional. The data model is simpler, but query options and metadata support are more limited.

[[OData V4]] is the modern successor with extended capabilities. [[JSON]] is the default format, and performance is improved through advanced query options such as filters, aggregation, and navigation. In addition, V4 introduces support for actions, functions, and batch processing, along with enhanced features for authorisation and security.

In the Tchibo context, many existing [[SAP Fiori]] applications and older [[SAP]] systems still rely on [[OData V2]], while new solutions based on [[SAP S/4HANA]] are consistently created with [[OData V4]]. New applications should always be developed using the V4 protocol version.