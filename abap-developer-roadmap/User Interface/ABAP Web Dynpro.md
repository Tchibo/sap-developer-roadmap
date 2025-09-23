#Basic 

ABAP Web Dynpro (WD4A) is a stateful, server side UI technology for rendering in web browsers. 'Stateful' refers to the fact that the ABAP application server keeps track of the state of a user session between user interactions, 'server side' refers to the fact that UI components are processed on the server to create html before it is sent to the client's browser for rendering. Backend requests from the WD4A UI to the ABAP Platform transport the UI definition in the form of HTML and the data that needs to be rendered.

WD4A is a UI framework designed for desktop use, it lacks responsiveness and mobile-friendly features, it is not able to run offline and thus leads to poor user experience on smaller, mobile touch screens. 

There is no use case justifying the creation of new, custom build WD4A UIs. We support WD4A applications that are shipped by SAP but we do not implement new UIs using WD4A.

## Further reading
#article [SAP Standard ABAP Web Dynpro applications](https://pr.alm.me.sap.com/launchpad#FALApp-display&/?sap-iapp-state=AS45FB4PMQQMHMZYCT7TFPCDCH9K6IOF5JO7I4BX)
