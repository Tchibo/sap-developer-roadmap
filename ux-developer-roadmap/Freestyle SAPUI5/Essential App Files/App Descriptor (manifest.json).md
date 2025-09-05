#Advanced

The `manifest.json` file is a central repository for metadata in SAP applications, components, or libraries, inspired by the W3C's WebApplication Manifest concept. It provides a machine-readable format to define app behavior and requirements.

-  **Versioning:** Features a `_version` attribute for manifest version control, ensuring compatibility with various SAPUI5 versions like `1.2.2` or `1.73.1`.

-  **Localization:** The `i18n` attribute specifies a properties file URL or object for text symbols, essential for multilingual support and UI adaptation to different languages.

-  **IDs for Applications and Components:** The `id` attribute assigns unique identifiers to project components, preventing conflicts and aiding navigation. IDs are in dot notation for uniqueness.

-  **Integration and Dependencies:** Lists necessary libraries or components with attributes like `minUI5Version` to ensure functionality, detailing lazy loading options for performance optimization.

-  **Embedding Components:** Attributes like `embeds` and `embeddedBy` define nested `manifest.json` paths, aiding in managing multi-component applications.

-  **Types of Applications:** The `type` attribute classifies projects as applications, components, libraries, or cards, specifying their roles within the SAP environment.

Overall, `manifest.json` serves as a blueprint for detailing resources, behaviors, version compatibility, and localization strategies, ensuring efficient operation and adaptability across environments.
## Further Reading

- #Article [App Initialization: What Happens When an App Is Started?](https://sapui5.hana.ondemand.com/#/topic/d2f58695fce3476f92fdfc07c9e8f7c6)
- #Article [App Overview: The Basic Files of Your App](https://sapui5.hana.ondemand.com/#/topic/28b59ca857044a7890a22aec8cf1fee9)
- #Course [Folder Structure: Where to Put Your Files](https://sapui5.hana.ondemand.com/#/topic/003f755d46d34dd1bbce9ffe08c8d46a)
- #Course [Manifest (Descriptor for Applications, Components, and Libraries)](https://sapui5.hana.ondemand.com/#/topic/be0cf40f61184b358b5faedaec98b2da)
- #Course [Development Guide: Descriptor for Applications](https://sapui5.hana.ondemand.com/#/topic/8f93bf2b2b13402e9f035128ce8b495f)