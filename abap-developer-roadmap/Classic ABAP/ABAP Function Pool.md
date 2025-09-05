#Basic
An ABAP function pool is a special type of ABAP program that was developed to encapsulate reusable procedures, known as function modules. Function modules allow a certain degree of encapsulation of business logic, making it reusable in multiple applications within the SAP system. Each function pool is linked to a function group that contains related function modules. This organization helps maintain modularity and improve code readability.

Function pools are characterized by the fact that they manage global data declarations that can be accessed by all function modules within the same group. This feature enables data to be exchanged between function modules, thereby reducing redundancies. Function modules within a pool can be called remotely (RFC) and locally.

RFCs will continue to be relevant in hybrid system landscapes or for step-by-step data migrations in the future, but SAP is increasingly focusing on modern API technologies and Event-driven Architecture.

### Useful Links
- #Article [Function Modules](https://help.sap.com/doc/saphelp_nw73ehp1/7.31.19/en-us/d1/801ea7454211d189710000e8322d00/content.htm?no_cache=true)
- #Article [Definition Function Modules](https://help.sap.com/doc/abapdocu_752_index_htm/7.52/en-us/abenabap_functions.htm)
- #Article [Function Groups](https://help.sap.com/doc/saphelp_snc700_ehp01/7.0.1/en-us/9f/db992335c111d1829f0000e829fbfe/content.htm?no_cache=true)
- #Article [RFC Function Modules](https://help.sap.com/docs/SAP_NETWEAVER_700/108f625f6c53101491e88dc4cf51a6cc/48920827feb35ed2e10000000a42189d.html?locale=en-US)
- #Article [Different Types of  RFC Calls](https://community.sap.com/t5/application-development-and-automation-blog-posts/understanding-different-types-of-rfc-calls-in-sap-abap/ba-p/13745585)

