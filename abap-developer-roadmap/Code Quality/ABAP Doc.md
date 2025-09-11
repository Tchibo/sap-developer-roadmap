#Basic 
SAP ABAP Doc is a documentation tool for ABAP developers that provides structured inline documentation for ABAP source code objects such as classes, methods, function modules and interfaces. Its main purpose is to improve the understandability and maintainability of code by enabling developers to describe code functionality, usage, parameters, exceptions and results directly within the code base in a standardised and readable format.

>You can use quickfixes (Ctrl+1) within an ABAP Doc comment block to generate templates for all parameters and exceptions that have not yet been documented.

```
"! Method to check if two sources are identical
"! @parameter source1     | First source
"! @parameter ignore_case | Pass abap_true to ignore case
"! @parameter result      | Returns abap_true if sources are identic
"! @raising cx_aab_static | One of the sources is empty
METHODS method_with_variable
IMPORTING
 source1 TYPE text
 ignore_case TYPE abap_bool DEFAULT abap_false
RETURNING
 VALUE(result) TYPE abap_bool
RAISING
 cx_aab_static.
```

With the additions "shorttext synchronized" and "lang = ...", the texts are uploaded to the repository in the respective language and can also be seen in the SE80.

``` 
<p class="shorttext synchronized" lang="en">...</p> 
```
 
The ABAP Doc is used for the element info (F2) or for auto-completion in Eclipse.
# Resources

#website [ABAP Doc - ABAP-Schlüsselwortdokumentation](https://help.sap.com/doc/abapdocu_750_index_htm/7.50/de-de/abendoccomment.htm)
#Article [ABAP Doc - SAP Community](https://community.sap.com/t5/application-development-and-automation-blog-posts/abap-doc/ba-p/13223459)
#course [Documenting ABAP Code](https://learning.sap.com/learning-journeys/acquire-core-abap-skills/documenting-abap-code_ad565c7e-6ac5-4a49-95e2-e4c33268dac6)