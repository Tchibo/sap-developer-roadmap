---
tags:
  - basic
links:
  - "[[CDS Profiles]]"
  - "[[Security]]"
  - "[[Roles]]"
  - "[[Role-Collections]]"
  - "[[Testing]]"
source:
aliases:
---
Developers can mock users in the local [[CDS]] configuration in [[SAP Capire]] to simulate different authentication scenarios. Mock users can be assigned usernames, passwords, roles, and attributes, which are then available in the application logic for authorization checks. This is valuable for testing role-based access controls and verifying that features are accessible only to users with the correct permissions.

Using mock users allows developers to efficiently validate application security during local development without complex authentication setups.

**Example**  
To mock users, add a `cds.requires.auth.users` section to your `package.json`:
```json
{
  "cds": {
    "requires": {
      "auth": {
        "users": {
          "alice": { "password": "alicepwd", "roles": ["admin"] },
          "bob": { "password": "bobpwd", "roles": ["user"] }
        }
      }
    }
  }
}
```
In this example, "alice" has the "admin" role, and "bob" has the "user" role.

**Summary**  
Mock users in local [[CDS]] configuration allow developers to simulate user authentication and authorization, making it easy to test access control during development.

**Sources**
- [SAP Capire - Mock users](https://cap.cloud.sap/docs/node.js/authentication#mock-users)
- [SAP Capire - Toggle Features](https://cap.cloud.sap/docs/guides/extensibility/feature-toggles#in-development)
- [SAP Capire - Enable Feature Toggles](https://cap.cloud.sap/docs/guides/extensibility/feature-toggles#enable-feature-toggles)  