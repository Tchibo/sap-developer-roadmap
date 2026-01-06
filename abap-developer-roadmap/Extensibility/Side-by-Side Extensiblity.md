#Basic 

**Side-by-side extensibility** refers to an approach in which extensions and custom applications are implemented outside the core SAP systems. This keeps the SAP core free of extensions (also referred to as *clean*) and ensures easier upgrades, while mitigating the stability risks associated with creating direct (**on-stack**) extensions.

Side-by-side extensibility leverages SAP BTP’s evolving suite of innovative cloud services, enabling business process changes without compromising the stability of core system processes.

Side-by-side extensions are typically full-stack applications. They use connectivity services to consume data from core SAP systems running on-premise or in public or private cloud environments. Such extensions are implemented either using the **Cloud Application Programming Model (CAP)** or the **RESTful Application Programming Model (RAP)**.

CAP solutions run on SAP BTP Cloud Foundry or Kyma runtimes and are developed using SAP Build Code. RAP solutions run in the BTP ABAP environment or on on-premise ABAP systems and are developed using Eclipse ABAP Development Tools (ADT) and SAP Build Code.

To ensure that side-by-side extensions remain upgrade-stable with respect to the core SAP systems they extend, only **released** SAP standard APIs or **released custom APIs** created on-stack must be consumed.
## Further reading

#Article [Explaining Side-by-side Extensiblity (ABAP)](https://learning.sap.com/learning-journeys/practicing-clean-core-extensibility-for-sap-s-4hana-cloud/explaining-side-by-side-extensibility_a01bb1ac-1acb-434d-8458-7a36cf2bcb3b)



