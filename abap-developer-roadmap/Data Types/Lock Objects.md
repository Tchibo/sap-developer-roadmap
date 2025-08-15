Lock objects secure a database table during data modification by a program. This prevents inconsistencies that would arise if multiple users or programs attempted to alter the same entry simultaneously.
Locks are synchronized between application servers of the same system. They can also be used to easily prevent simultaneous runs of background jobs. Locks are requested explicitly in code and can be released manually, otherwise they are released at the end of the transaction.
# Optimistic Locks
These are used in Fiori apps. They allow multiple users to display data in editable mode (competing locks). The first to actually make changes wins. All other users have to refresh the data before being able to make changes again. 
# Exclusive Locks
The most common type in SAP GUI transactions is exclusive locks to update data. Whenever data is changed, an exclusive write lock must be acquired and it should be as specific as possible.
Locks are set and removed by calling the enqueue and dequeue function module, which is generated automatically when creating a lock object.
```abap
CALL FUNCTION 'ENQUEUE_EMMARA'
  EXPORTING
    mode_mara     = 'E'          " E = Exclusive, S = Shared
    ...
  EXCEPTIONS
	...
    OTHERS        = 3.
```
#### Resources
#website [SAP Lock Concept](https://help.sap.com/docs/ABAP_PLATFORM_NEW/6568469cf5a1460a8d85c58b83d21ec2/47df116e6abf296fe10000000a42189b.html?locale=en-US)
#website [SAP Help Portal | Lock Objects](https://help.sap.com/docs/ABAP_PLATFORM_NEW/ec1c9c8191b74de98feb94001a95dd76/cf21eea5446011d189700000e8322d00.html?locale=en-US)
#article [Data Flair | Lock Objects in SAP ABAP – Types and Examples](https://data-flair.training/blogs/lock-objects-in-sap-abap-types-and-examples/)