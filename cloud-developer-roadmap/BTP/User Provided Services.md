---
tags:
  - sap-btp
  - Basic
links:
  - "[[SAP BTP]]"
  - "[[Service Bindings]]"
  - "[[Cloud Foundry]]"
  - "[[cf CLI]]"
source: https://help.sap.com/docs/btp/sap-business-technology-platform/creating-user-provided-service-instances
aliases:
  - ups
---
User Provided Services (UPS) are service instances in the [[Cloud Foundry]] environment of [[SAP BTP]] that are created and filled with credentials by the developer or operator. In contrast to managed services from the SAP BTP service marketplace, the platform does not provision the external resource itself. The UPS only stores the connection information that an application needs.

A UPS is used when an application has to consume a service that is not available as a managed service instance in the current space, for example an external API, an existing database, an on-premise endpoint, or a technical service with manually provided credentials. After the UPS has been created, it can be bound to an application like other service instances. The application then receives the credentials through the Cloud Foundry service binding mechanism, usually via the `VCAP_SERVICES` environment variable.

This approach keeps connection data out of the application code and makes it possible to manage endpoint URLs, users, passwords, tokens, or other service-specific properties as part of the platform configuration.

**Example**
Create a user provided service instance with the [[cf CLI]]:

```sh
cf create-user-provided-service my-external-api -p '{
  "url": "https://api.example.com",
  "clientid": "my-client-id",
  "clientsecret": "my-client-secret"
}'
```

The short form of the command is:

```sh
cf cups my-external-api -p '{
  "url": "https://api.example.com",
  "clientid": "my-client-id",
  "clientsecret": "my-client-secret"
}'
```

Afterwards, the service instance can be bound to an application:

```sh
cf bind-service my-application my-external-api
```

**Sources**
- [SAP Help Portal - Creating User-Provided Service Instances](https://help.sap.com/docs/btp/sap-business-technology-platform/creating-user-provided-service-instances)
