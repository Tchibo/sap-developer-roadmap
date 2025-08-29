### Authentication
**Authentication** is the process of verifying the identity of a user or a system in order to grant access to a certain resource. 

In the context of outbound or inbound communication to ABAP application server relevant methods are
- basic authentication (user & password)
- client certificates (TLS / mTLS)
- open Authorization (oAuth v2).

At least when interacting with Cloud services, integrations must not use basic authentication.
### Authorization
**Authorization** define user **permissions** after authentication. Within ABAP Platform this is done by  authorization objects and values which are being put into roles that are assigned to a user.

Authorizations are especially relevant for inbound communication were its necessary to determine which rights a user has to create, change, delete or read a certain information. For the inbound case the authorizations needs to be restricted. 

