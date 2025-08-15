**A Number Range Object** is a SAP configuration that maintains a persisted counter value used for ID generation. Each time a new ID is requested, the counter is incremented and the new value is returned.

Number Range Objects automatically generate (**"internal assignment"**) unique, sequential identifiers (numeric or alphanumeric) within specified ranges. They are widely used throughout SAP modules for Products, Invoices, Sales Orders, and many other business objects.

Alternatively, number ranges support **"external assignment"** where users or external processes provide the number, and the system validates uniqueness within the defined range.

Generated numbers are unique locally: Within the specific client and SAP system, uniqueness is guaranteed by the ABAP Platform. In contrast to UUIDs, they are human-readable, usually sequential and may have semantic meaning attached to their ranges.

To get a new number for a given number range, call Function Module `NUMBER_GET_NEXT`.
### Resources
#website [SAP BTP | Number Ranges](https://help.sap.com/docs/btp/sap-business-technology-platform/number-range-solution?locale=en-US&version=LATEST)
#course  [Number Range Creation - Step by Step](https://sapcodes.com/2016/11/19/number-range-object-2/)
#video[Number Range Creation and Usage](https://www.youtube.com/watch?v=mRAMszU9S3s)