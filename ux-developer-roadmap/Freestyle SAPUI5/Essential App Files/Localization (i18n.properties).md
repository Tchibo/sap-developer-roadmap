#Basic

The `i18n.properties` files are vital for localizing text within SAPUI5 applications. They contain key-value pairs that allow for translation in multiple languages, ensuring the application is accessible to a global audience. For instance, the English file might contain entries like:

```PROPERTIES
lastname=Last Name:
firstname=First Name:
email=Email:
submitButton=Submit
```
Here, each key (such as `welcome`, `lastname`) corresponds to a user interface element, providing text content in English. The `{0}` in the `welcome` message acts as a placeholder for dynamic data insertion, allowing personalized greetings. In contrast, the German file (`i18n_de.properties`) would have:

```PROPERTIES
lastname=Nachname:
firstname=Vorname:
email=E-Mail:
submitButton=Absenden
```

This ensures that the same keys show translated text for German users, maintaining consistency in UI element functionality across languages.

The `ResourceBundle` acts as the access point for these translations, dynamically loading the correct `i18n.properties` file during runtime based on the locale settings. Developers use methods like `getText` to retrieve values associated with keys, enabling the application to display language-specific content without changing the underlying code.

By employing a `ResourceBundle`, applications achieve seamless localization, allowing for real-time language changes and personalized interaction. This structure ensures efficient and flexible multilingual support, enhancing usability and accessibility for global users without necessitating extensive engineering changes.
## Further Reading

- #Website [Localization](https://sapui5.hana.ondemand.com/#/topic/91f217c46f4d1014b6dd926db0e91070)
-  #Course [Resource Bundles](https://sapui5.hana.ondemand.com/#/topic/91f225ce6f4d1014b6dd926db0e91070)