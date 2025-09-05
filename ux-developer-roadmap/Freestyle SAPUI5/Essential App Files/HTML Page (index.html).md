#Basic 

The `index.html` file in an SAPUI5 application acts as the entry point for standalone apps, enabling the setup and initialization of the application environment. It declares the document type as HTML5 and sets the primary language to English. This file includes meta tags for character encoding, responsive design, and compatibility, while setting the page `<title>`. Styles ensure dynamic layouts by occupying full height for elements like `html` and `body`.

A key feature is the SAPUI5 bootstrap `<script>`, which loads necessary libraries from a local `resources` directory, sets the theme to e.g. `sap_fiori_3`, and defines application settings such as async behavior and component support for modern compatibility (e.g. `compatVersion="edge"`). The body section incorporates SAPUI5 styling and configures a div to instantiate a component (More under Components Subtopic), which handles the business logic and UI rendering.

While SAP Fiori launchpad apps do not require an `index.html` file, standalone apps use this file to configure their environment independently, offering flexibility for testing and development by running and debugging outside of FLP, ensuring that SAPUI5 libraries are correctly loaded and linked to the application interface.
## Further Reading

- #Article [App Initialization: What Happens When an App Is Started?](https://sapui5.hana.ondemand.com/#/topic/d2f58695fce3476f92fdfc07c9e8f7c6)
- #Article [App Overview: The Basic Files of Your App](https://sapui5.hana.ondemand.com/#/topic/28b59ca857044a7890a22aec8cf1fee9)
- #Course [Folder Structure: Where to Put Your Files](https://sapui5.hana.ondemand.com/#/topic/003f755d46d34dd1bbce9ffe08c8d46a)