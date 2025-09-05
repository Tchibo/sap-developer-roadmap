#Advanced 

The `mta.yaml` file serves as a blueprint for constructing and deploying a Multi-Target Application (MTA) in SAP's Cloud Platform. It defines modules, resources, and dependencies for an application spanning different technologies, such as HTML5 and Java.
### Building Process:

1. **Configuration**: Within the `mta.yaml`, developers specify modules, resources, and dependencies.

2. **Build Execution**: Using the SAP MTA Build Tool (`mbt`), the configuration is processed to package application components into an `.mtar` file, a deployable archive format. This tool reads the `mta.yaml` to ensure all components are built according to defined parameters, compiling source code and bundling necessary resources.
### Deployment Process:

1. **Deployment Tool**: The `Cloud Foundry CLI` or SAP Business Application Studio is used for deployment purposes.

2. **Deployment Execution**: The `.mtar` file is deployed to SAP Cloud Platform, orchestrating the setup of modules and allocation of resources. The deployment tool interprets the configurations in the `.mtar` to establish connections and activate services specified in `mta.yaml`.
## Further Reading

- #Course [Working with the Mta.yaml File](https://learning.sap.com/learning-journeys/develop-advanced-extensions-with-sap-cloud-sdk/working-with-the-mta-yaml-file_a884b953-7212-439d-a5f0-5c3fd122f75f)