The ABAP Dictionary (also known as **Data Dictionary** or **DDIC**) is a central SAP tool for defining and managing data types. Data types defined here are reusable across an ABAP system but typically serve specific contexts or use cases. The Dictionary also includes reusable definitions such as **Structures** and **Table Types**.
**Built-In Elementary Data Types** exist both within the Dictionary and directly in ABAP code. Values can convert losslessly between these, though definitions slightly differ.

### Domain
Domains are simple data types derived from **Built-In Elementary Data Types**, specifying type and length. Example: MATNR, type char, length 40, universally represents material numbers within SAP.

### Data Element
A data element references a **Domain** or **Built-In Elementary Data Type** and defines both technical properties and semantic meaning, tailored to specific applications or use cases.

### Database Table
Database tables store persistent data in SAP, including business data, customizing settings, and code. ABAP SQL or CDS views can only access tables defined in the Dictionary (**transparent tables**). These tables exist both as ABAP structures and physically in the database, with at least a primary key and optionally secondary keys.

### Resources
#website [SAP Help Portal | ABAP Dictionary](https://help.sap.com/docs/ABAP_PLATFORM_NEW/ec1c9c8191b74de98feb94001a95dd76/cf21ea0b446011d189700000e8322d00.html?locale=en-US&version=LATEST)
#website [ABAP Cheat Sheets | ABAP Dictionary](https://github.com/SAP-samples/abap-cheat-sheets/blob/main/26_ABAP_Dictionary.md)
#article [SAP Blog: Data Dictionary Introduction](https://community.sap.com/t5/application-development-and-automation-blog-posts/getting-started-with-abap-data-dictionary-introduction/ba-p/13521855)
#course  [SAP Learning | Data Dictionary in Eclipse](https://developers.sap.com/tutorials/abap-dev-learn-ddic..html)
#course [Ducat | ABAP Data Dictionary](https://tutorials.ducatindia.com/sap-abap/sap-data-dictionary)