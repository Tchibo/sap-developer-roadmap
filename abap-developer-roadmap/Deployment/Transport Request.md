#Basic 

> [!todo] Gekürzt
> Ich habe auch diesen Text gekürzt (268 -> 204 Worte), passt das für dich?

Within the ABAP Environment transport requests serve as the deployment mechanism to move development artifacts and configuration from development to quality assurance and production. Changes to transportable content are disallowed in quality assurance and production, ensuring there is only one original system for configuration or repository objects.

Types of transport requests include workbench requests for repository objects, customizing requests for client-dependent setups, repairs for alterations to SAP standard, and the advanced type transport of copies, essential in quality assurance processes.

A transport request comprises one request and one or more tasks, each assigned to a user. In development, transportable content created or changed by a user is automatically recorded in that user’s task. When a **task** is released, its objects move to the main **request**. Versioning of ABAP repository objects occurs when a transport request is released, with each release adding an entry to the object’s version history.

Repository objects are locked once added to a transport request to prevent concurrent modifications, though multiple developers can still collaborate by working within shared tasks of the same request. This enables group work while ensuring accountability.

Transport requests underpin Change Request Management (ChaRM), supporting repeated deployment to quality assurance via transports of copies during functional testing.

## Further reading

#Article [Transport Request](https://help.sap.com/docs/abap-cloud/abap-development-tools-user-guide/transport-request)

