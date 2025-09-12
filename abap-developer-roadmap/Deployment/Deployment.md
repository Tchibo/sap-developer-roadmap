#Basic 

Deploying ABAP development objects across a typically 3 tier landscape that includes development, test, and production systems is essential for ensuring governance and system stability in production environments. Each ABAP object originates in the development system, where developers can design, code and do technical unit test. Once objects in development are mature, they are transported to the test system to undergo functional testing for validation against business requirements without perturbing live operations. After successful testing, the objects are deployed to the production system, where they support daily business processes with stability and reliability. 

For an **On-Premise** SAP system landscape the SAP Change and Transport System (CTS) facilitates transport of ABAP objects between systems, ensuring that all changed objects are included and that versioning of repository objects are tracked. Additionally, SAP Solution Manager with its Change Request Management (ChaRM) feature provides oversight and control over transport requests, running checks and balances and managing complexity in transport sequencing. 

## Further Reading
#Article [Change and Transport System](https://help.sap.com/docs/ABAP_PLATFORM_NEW/4a368c163b08418890a406d413933ba7/3bdfba3692dc635ce10000009b38f839.html?locale=en-US)
