#Advanced 
The controlled SAP LUW enhances the standard SAP LUW concept in both ABAP Cloud and classic ABAP by introducing check mechanisms to detect transactional contract violations and ensure consistency.

**Key Features:**
- Defines which ABAP statements are allowed/forbidden in specific transactional phases
- Detects violations that result in runtime errors or logging
- Makes applications more robust and the SAP LUW more tangible

**Transactional Phases:**
- Modify phase - includes RAP interaction and early save phases
- Save phase - includes RAP late save phase

Phases can be activated explicitly using `CL_ABAP_TX=>modify()` and `CL_ABAP_TX=>save()` methods by developers, or implicitly through newer ABAP concepts like RAP, Background Processing Framework, and RAP Business Events.

```
"Setting the modify transactional phase.
...
cl_abap_tx=>modify( ).
...
"After the modify transactional phase is started, the following statement is a violation.
"MODIFY dbtab FROM @row.

"Setting the save transactional phase.
...
cl_abap_tx=>save( ).
...
"After the save transactional phase is started, database modification operations are allowed.
MODIFY dbtab FROM @row.
```

**Transactional Contracts:** APIs are classified with interfaces like `IF_ABAP_TX_SAVE`, restricting their usage to appropriate phases. For example, `CL_BCS_MAIL_MESSAGE->send_async()` cannot be called during the modify phase.

**Common Violations:**
- Database modifications in modify phase (only allowed in save phase)
- Calling classified APIs in wrong phases
- Database changes in RAP handler methods without proper phase activation

This controlled approach ensures data consistency by preventing operations when data might be in an inconsistent state.

### Useful Links
- #Article  [Controlled SAP LUW](https://help.sap.com/docs/abap-cloud/abap-concepts/controlled-sap-luw?locale=en-US)