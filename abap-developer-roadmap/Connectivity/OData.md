#basic
Developed by Microsoft, the **Open Data Protocol (OData)** is an open standard for REST-based data access via HTTP. It is built upon core REST principles, which ensure resource-oriented URLs and the correct use of HTTP verbs (GET, POST, etc.) for each action.

The protocol provides a set of common rules to standardize request patterns. This includes uniform query options for common tasks like paging (`$top`, `$skip`), filtering (`$filter`), and sorting (`$orderby`).

Its primary benefit lies in exposing backend data in a standardized, queryable, and discoverable way, significantly reducing the custom code needed on both client and server. This makes OData the standard choice for custom development, since it perfectly suited for building synchronous web API's as well as UI services for SAP Fiori. These can be set up based on Core Data Services as well as Restful Application Programming.

 While the older V2 version was widely used in the past, the new V4 version offers a range of advantages, including better metadata compression and more sophisticated query, sorting, and filter mechanisms. therefore only the newer v4 version should be used.

```
    "results" : [  
      {  
        "__metadata" : {  
          "id" : "http://xxx.xxx.xxx.net:xxx/sap/opu/odata/SAP/ZVBST_ART_SRV/ArticleSet('600')",  
          "uri" : "http://xxx.xxx.xxx.net:xxx/sap/opu/odata/SAP/ZVBST_ART_SRV/ArticleSet('600')",  
          "type" : "ZVBST_ART_SRV.Article"  
        },  
        "articleId" : "600",  
        "name" : "RA PK Latin Grande 250gx2 xx",  
        "sort" : "Tchibo Privatkaffee",  
        "barcode" : "4006067006005",  
        "startOfValidity" : "\/Date(1325376000000)\/",  
        "endOfValidity" : "\/Date(253370678400000)\/",  
        "creationDate" : "\/Date(1368662400000)\/"  
      },
...
```
### Usage

### Ressources
[ODATA V4 | SAP S/4HANA Cloud Private Edition | SAP Business Accelerator Hub](https://api.sap.com/products/SAPS4HANACloudPrivateEdition/apis/ODATAV4)
[SAP Gateway Foundation Developer Guide (v2) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/a6422751c639276ee10000000a445394.html?locale=en-US)
[SAP Gateway Foundation for OData V4 Developer Guide | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/1bbc4ecf0da94f358b1355fcbffa3363.html?locale=en-US)
[OData Request System Query Options | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/64efa736927c4850aea8e9c2683df6cf.html?locale=en-US)

Nicht hilfreich, da Gateway Service Builder - aber vielleicht nochmal zum Gateway verstehen:
[Building OData Services with SAP Gateway | SAP Learning](https://learning.sap.com/learning-journeys/building-odata-services-with-sap-gateway)