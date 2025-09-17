#basic
Destinations are the construct where endpoints as well as authentication information is  stored or referenced. Typically this is done via transaction `SM59`, which is widely used within SAP.
The following destination types can be administered here
- HTTP Destinations 
- RFC / ABAP Destinations
- registered Server Programs
- Channel endpoints 
##### Other Transactions
`SOAMANAGER` is used to maintain endpoints as well as authorization information for SOAP services. 

`OA2C_CONFIG` is used to maintain oAuth configurations in order to be used for authorization usage during data exchange. While the oAuth Konfig is maintained in `OA2C_CONFIG`, it is referenced in the destination definition of transaction  `SM59`.