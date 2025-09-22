#Basic 

Web GUI (also know as HTML GUI) is a stateful, server side UI technology for rendering ABAP dynpro based transactions as HTML in web browsers. 'Stateful' refers to the fact that the ABAP application server keeps track of the state of a user session between user interactions, 'server side' refers to the fact that UI components are processed on the server to create html before it is sent to the client's browser for rendering. Backend requests from the Web GUI to the ABAP Platform transport the UI definition in the form of HTML and the data that needs to be rendered.

Web GUI is a 'stop-gap' UI technology to allow ABAP Dynpro based transactions and their UI to be consumed through web browsers. The Internet Transaction Server (ITS) that is part of the ABAP Platform kernel translates the ABAP dynpros to HTML at runtime. The ITS is a service in the Internet Communication Framework of the ABAP Platform and responds on service path /sap/bc/gui/sap/its/webgui.

## Further reading
#article [Web GUI and Internet Transaction Server](https://help.sap.com/docs/SUPPORT_CONTENT/uiwits/3361892170.html?locale=en-US)

