#Basic 

> [!TODO] Review Comment
> - Grundsätzlich wichtiger Inhalt! Allerdings hätte ich bei diesem Subtopic eher erwartet, dass es spezifischer auf die Struktur eines Fiori Elements Repositories eingeht, also die tatsächliche File Struktur und welche Ordner für den Entwickler wichtig sind. Wie z.B der "annotations"-Ordner oder die `mta.yaml`-Datei
> - MVC ein sehr großes Thema evtl zu groß für ein kleines Subtopic, welches auch noch andere Themen aufgreift? (Wenn es drin bleiben soll würde ich definitiv auch eine Doku dazu verlinken z.B. diese hier: [GUI Architectures](https://martinfowler.com/eaaDev/uiArchs.html#ModelViewController))
> - Sind Smart Controls unter Fiori Elements zu verordnen? Sehe das eher bei Freestyle, da ja auch die OData V4 Kompatibilität nur teilweise gegeben ist

The architecture of SAP Fiori Elements consists of a frontend built using HTML5 and JavaScript, combined with OData services. Fiori Elements is designed to operate within the SAPUI5 framework, leveraging SAP's robust client-server architecture to ensure high performance and scalability.
The frontend utilizes the model-view-controller (MVC) paradigm, where:
- **Model**: Represents the data sourced through OData.
- **View**: Defined by pre-built templates and smart controls for consistent UI.
- **Controller**: Governs the interaction between the model and view, albeit simplified in Fiori Elements where annotations play a significant role.

The communication between backend and frontend occurs via OData services, ensuring a smooth data flow for efficient application response times.
### Key Components of SAP Fiori Elements
1. **Annotations**: These are metadata used to define the UI and behavior of apps without additional coding.
2. **OData Services**: SAP Fiori Elements rely heavily on OData services to retrieve and manipulate data. These services expose data that Fiori applications can consume, prioritizing a model-driven design.
3. **Templates**: SAP provides standard templates for various application types such as List Report, Object Page, Worklist, and Overview Page. These templates come pre-configured with common functionalities like filtering, searching, and data visualization.
4. **Smart Controls**: Integrated into Fiori Elements, smart controls are UI elements designed to automatically adapt according to the application context, utilizing annotations to determine behavior and appearance.
### Useful Links
- #Article [Architecture of SAP Fiori Elements](https://learning.sap.com/learning-journeys/develop-sapui5-applications/explaining-the-architecture-of-fiori-elements_e89bd7ac-24e6-4b46-a84e-8011c612a37e)