#Basic 

> [!todo] Gekürzt
> Ich habe den Text halb-manuell/halb-ChatGPT gekürzt (236 Wörter zu 193 Wörter) und dabei versucht, nichts wegzulassen. Passt das für dich?

Change Request Management (ChaRM), an offering of the SAP Solution Manager, manages the software development lifecycle from implementation through testing to deployment.

A change request in ChaRM bundles transport requests containing transportable content created or changed in development systems. It validates the transport content to prevent side-effects and orchestrates transport execution, ensuring a clear separation of responsibilities among consultants, project managers, and developers.

A change request starts with the action 'Set status to in development'. Developers can then create and append transport requests in the development system, allowing multiple contributors to record and collaborate on changes.

Once development is ready for testing, all tasks in the transport requests must be manually released. Triggering 'Hand over to functional unit test' initiates a 'transport of copies' to the quality assurance system. During release, ChaRM performs code quality checks using the default ABAP Test Cockpit profile.

Upon successful testing by the functional consultant, 'Confirm successful testing' releases all transport requests associated with the change request. The following action 'Import to production' deploys them into the production system. ChaRM performs transport-related validations to shield target systems from out-of-sequence imports or downgrades, thereby preventing syntactical and functional errors.

## Further reading

#Article [Change Request Management](https://help.sap.com/docs/SAP_Solution_Manager/8b923a2175be4939816f0981b73856c7/4c3acb82b50843b4e10000000a42189e.html?locale=de-DE)
