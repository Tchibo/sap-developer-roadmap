- [ ] #todo Advantages of OData in general
- [ ] #todo Mention CDS & RAP?
- [ ] #todo OData = standard way to go for custom developments

**Open Data Protocol (OData)** is an open standard developed by Microsoft as REST based data access via HTTP.  REST ensures resource-oriented URLs and the correct use of HTTP verbs (GET, POST, etc.) for each action. OData builds on this and standardizes the request pattern, adding uniform query options for paging (`$top`, `$skip`), filtering (`$filter`), and sorting (`$orderby`).

OData is provided in two versions: V2 was widely used in the past.
=> Offen: hat V2 noch eine Daseinsberechtigung abseits das es nicht alle Standard APIs als V4 gibt? Check gen Arjo

The new version V4 provides a bunch of advantages like better metadata compression, more sophisticated queries, sorting and filter mechanisms. 

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
OData can and should be used in cases were a synchronous access on data in SAP systems is needed. Newly developed oData's should always be set up in version 4.

=> Macht hier die Unterscheidung Inbound / Outbound wirklich Sinn?
odata - way to go for inbound, outbound ggf. REST ? 
Erläuterung Inbound & Outbound - von SAP zu SAP

### Ressources
[ODATA V4 | SAP S/4HANA Cloud Private Edition | SAP Business Accelerator Hub](https://api.sap.com/products/SAPS4HANACloudPrivateEdition/apis/ODATAV4)
[SAP Gateway Foundation Developer Guide (v2) | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/a6422751c639276ee10000000a445394.html?locale=en-US)
[SAP Gateway Foundation for OData V4 Developer Guide | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/1bbc4ecf0da94f358b1355fcbffa3363.html?locale=en-US)
[OData Request System Query Options | SAP Help Portal](https://help.sap.com/docs/ABAP_PLATFORM_NEW/68bf513362174d54b58cddec28794093/64efa736927c4850aea8e9c2683df6cf.html?locale=en-US)

Nicht hilfreich, da Gateway Service Builder - aber vielleicht nochmal zum Gateway verstehen:
[Building OData Services with SAP Gateway | SAP Learning](https://learning.sap.com/learning-journeys/building-odata-services-with-sap-gateway)