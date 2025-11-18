#Basic 

Classic extensibility and developer extensibility are different approaches to extending SAP systems. Classic extensibility offers maximum flexibility with no restrictions but can lead to upgrade challenges while developer extensibility leverages a cloud-ready, upgrade-stable ABAP development model with released APIs, promoting cleaner and more maintainable extensions. 

Characteristics of classic extensibility are:
- **Offers flexibility:** Offers maximum freedom and flexibility for extending the system. 
- **Has no restrictions:** There are no specific limitations on the extension model. 
- **Can lead to upgrade challenges:** due to the lack of clear interfaces between SAP code and extensions. 

Creating appends to non released dictionary structures or tables, extending CDS views, implementation of user exits (e.g. by means of transaction VOFM, or customer include MV45AFZZ), customer exits (defined in transactions SMOD and CMOD or Business Transaction Events using transaction FIBF), explicit and implicit enhancement spots or modification to SAP Standard form part of classic extensibility.

Classic extensibility techniques are to be avoided in favor of using developer extensibility options in order to safeguard a clean, seamlessly upgradeable core. 

## Further reading

#Article [Exploring the SAP S/4HANA Cloud Extensibility Model](https://learning.sap.com/learning-journeys/becoming-an-sap-btp-solution-architect/exploring-the-extensibility-of-sap-s-4hana)






