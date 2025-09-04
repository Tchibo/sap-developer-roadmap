Destinations are the construct where endpoints as well as authentication information are stored or referenced. Typically this is done via transaction SM59, which is widely used within SAP.
The following destination types can be administered here
- HTTP Destinations 
- RFC / ABAP Destinations
- registered Server Programs
- Channel endpoints 

The main transaction for the destination administration is the SM59. Here you can maintain endpoints as well as authentication information for the endpoints. Still there are other ways to store destinations which might also reference back to the SM59.
##### Other Transactions
SOAMANAGER is used to maintain endpoints as well as authorization information for SOAP services. OA2C_CONFIG is used to maintain oAuth configurations in order to be used for authorization usage during data exchange.

> [!NOTE] Anmerkung
> ADD Resources
