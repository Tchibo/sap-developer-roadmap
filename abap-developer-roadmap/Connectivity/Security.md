#intermediate 
### Authentication
**Authentication** is the process of verifying the identity in order to grant access to a certain resource. 

In the context of outbound or inbound communication relevant methods are
- basic authentication (user & password) 
- client certificates (TLS / mTLS)
- open Authorization (oAuth v2)
- Security Assertion Markup Language (SAML)
At least when interacting with Cloud services, integrations must not use basic authentication.
### Authorization
**Authorization** defines user **permissions** after authentication. Within ABAP Platform this is done by  authorization objects and values which are being put into roles that are assigned to a user.

Authorizations are especially relevant for inbound communication were its necessary to determine which rights a user has to create, change, delete or read a certain information. For the inbound case the authorizations needs to be restricted. 

### Functional User vs. Principal Propagation
The **Functional user** is a technical service account used for system-to-system communication. **Principal propagation** passes the actual end-user's identity through the entire call chain to the backend so that the authorizations of the user for the requested data can be checked.