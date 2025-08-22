**OData** is an open standard from SAP for REST-based data access via HTTP.

The newer version v4 has some major advantages over the older version2, which is no longer developed further, for example:
- Better metadata compression, thus saving 10% to 60% of the data volume.
- More sophisticated queries, sorting and filter mechanisms, and multi-level expands are supported, thus reducing the number of calls and data volume being transferred.
- Addition of advanced analytical capabilities to the set of possible queries.
- Ability of the client to access multiple services at the same time.
- Improved data types that suit the needs of business applications.

=> Compress
### Usage
OData can and should be used in cases were a synchronous access on data in SAP  systems is needed. Newly developed oData's should always be set up in version 4.

### Links
[ODATA V4 | SAP S/4HANA Cloud Private Edition | SAP Business Accelerator Hub](https://api.sap.com/products/SAPS4HANACloudPrivateEdition/apis/ODATAV4)
[SAP Gateway Foundation Developer Guide (v2) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/a6422751c639276ee10000000a445394.html?locale=en-US)
[SAP Gateway Foundation for OData V4 Developer Guide | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/1bbc4ecf0da94f358b1355fcbffa3363.html?locale=en-US)
[OData Request System Query Options | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/64efa736927c4850aea8e9c2683df6cf.html?locale=en-US)

Nicht hilfreich, da Gateway Service Builder - aber vielleicht nochmal zum Gateway verstehen:
[Building OData Services with SAP Gateway | SAP Learning](https://learning.sap.com/learning-journeys/building-odata-services-with-sap-gateway)