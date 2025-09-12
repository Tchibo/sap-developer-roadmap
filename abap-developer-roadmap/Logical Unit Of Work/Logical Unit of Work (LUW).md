#Intermediate 
A Logical Unit of Work (LUW) is one of the most fundamental concepts in SAP for ensuring data consistency. It represents a sequence of logically connected steps that must be executed as an inseparable, atomic unit. The principle is simple: all steps succeed, or no steps succeed. This "all-or-nothing" approach prevents the database from being left in a partial, inconsistent state if an error occurs mid-process.
Each opening of a new internal session starts a new SAP LUW (except the call dialog statement). The statements `COMMIT WORK` and `ROLLBACK WORK` determine the limits of an SAP LUW. An ABAP program can be divided into any number of SAP LUWs, whereby the end of an ABAP program always ends the last SAP LUW as well. All changes will be written on the database after a (implicit or explicit) `COMMIT WORK`.

### Useful Links
#Article [Data Consistency](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abendata_consistency.htm)
#Article [SAP LUW](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abensap_luw.htm)
#Article [Commit Work](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abapcommit.htm)
#Article [Implicit or explicit Commit Work](https://community.sap.com/t5/application-development-and-automation-discussions/what-is-the-functionality-of-explicit-commit-and-implicit-commit/m-p/2624439)
#Article [Rollback Work](https://help.sap.com/doc/abapdocu_latest_index_htm/latest/en-US/index.htm?file=abaprollback.htm)
#Article [What is LUW and how it works]([https://community.sap.com/t5/application-development-and-automation-blog-posts/what-is-luw-how-luw-works-different-types-of-luw/ba-p/13547262](https://community.sap.com/t5/application-development-and-automation-blog-posts/what-is-luw-how-luw-works-different-types-of-luw/ba-p/13547262))