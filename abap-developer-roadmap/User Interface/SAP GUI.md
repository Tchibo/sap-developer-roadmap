#Basic 

SAP GUI is a stateful, client side UI technology for rendering UIs in a locally installed application (the SAP GUI). 'Stateful' refers to the fact that the ABAP application server keeps track of the state of a user session between user interactions, 'client side' refers to the fact that UI components are processed on the client device to render the UI. Backend requests from SAP GUI to the ABAP application server use a SAP proprietary TCP/IP protocol connection and transport only the data that needs to be rendered. 

SAP GUI displays UIs that are built using ABAP Dynpro (dynamic programming) technology in the ABAP programming language, which runs on the SAP ABAP platform. The SAP GUI client application comes in two versions, **SAP GUI for Windows**: a desktop application for Windows systems and **SAP GUI for Java**: a platform-independent version written in Java. SAP GUI is designed for desktop use, it lacks responsiveness, cannot be executed on mobile devices, it is not able to run offline. 

Uses cases that justify to use SAP GUI is configuration in the SAP implementation guide or to use generated maintenance dialogs on custom configuration tables or view clusters. Using the SAP GUI is also indicated for submitting batch processing on custom built executable programs and to view the related application logs or list output. 

## Further reading
#article [SAP GUI](https://help.sap.com/docs/ABAP_PLATFORM_NEW/b1c834a22d05483b8a75710743b5ff26/9ad405e746ef43288755cb80a14be542.html)