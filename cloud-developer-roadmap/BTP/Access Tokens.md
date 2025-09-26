---
tags:
  - security
  - basic
links:
  - "[[SAP BTP]]"
  - "[[Service Bindings]]"
source:
aliases:
---
Access tokens are digital credentials used in modern authentication and authorization frameworks to grant temporary access to protected resources, APIs, or services without requiring re-authentication for every request.

**What Are Access Tokens?**
- Temporary authorization credentials for specific resources.
- Often formatted as [[JWT]] or opaque strings.
- Issued by an authentication server after successful login.
- Limited in scope and duration for security

**How They Work**
1. **Issuance** – After a user or application authenticates with an identity provider, the server issues a token.
2. **Content** – Includes issuer, audience, expiration, user identity, and permissions.
3. **Usage** – Sent in API calls via `Authorization: Bearer [token]`.
4. **Validation** – Checked for signature, expiry, and allowed scopes.
5. **Lifecycle** – Short-lived, renewable via [[Refresh Token]].

**Benefits**
- **Improved security** – No password sent each time.
- **Delegation** – Apps act on behalf of users.
- **Fine-grained access control** – Restrict to what’s needed.
- **Reduced authentication overhead** – Fewer logins.
- **Cross-service communication** – Secure service-to-service calls.    

Access tokens are central to [[OAuth 2.0]] and [[OpenID Connect]], forming the backbone of secure web and mobile authentication.

**Summary**  
Access tokens are short-lived credentials that allow secure, fine-grained, and delegated access to protected resources, making them essential for modern authentication and authorization frameworks.