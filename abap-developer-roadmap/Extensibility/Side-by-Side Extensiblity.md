#Basic 

**Side-by-side** extensibility refers to the approach where extensions and custom applications are implemented outside of core SAP systems. This keeps the core SAP systems free of extensions (also called 'clean') and ensures that they remain easier to upgrade while also mitigating the stability risks associated with creating direct (**on-stack**) extensions. 

Side-by-side extensibility has access to the potential of SAP BTP's evolving suite of innovative cloud services which allows to make innovative business process changes without compromising the stability of core system processes.

Side-by-side extensions are typically full-stack applications and make use of connectivity services to consume data from core SAP systems that run On-Premise or in the public or private cloud. They are implemented either as **Cloud Application Programming Model** (CAP) or **RESTful Application Programming Model** (RAP) solutions.

 CAP solutions run on the SAP BTP Cloud Foundry or Kyma runtimes and are created using SAP Build Code. RAP solutions run on the BTP ABAP Environment or the Tchibo On Premise ABAP Environment and are created using Eclipse ABAP Development Tools (ADT) and SAP Build Code. 

To ensure side-by-side extensions are upgrade stable in respect to the core SAP systems they extend, only released SAP standard APIs or custom APIs created on-stack must be consumed.

## Further reading

#Article [Explaining Side-by-side Extensiblity (ABAP)](https://learning.sap.com/learning-journeys/practicing-clean-core-extensibility-for-sap-s-4hana-cloud/explaining-side-by-side-extensibility_a01bb1ac-1acb-434d-8458-7a36cf2bcb3b)


