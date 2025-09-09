#Advanced 
The controlled SAP LUW enhances the standard SAP LUW concept in both ABAP Cloud and classic ABAP by introducing check mechanisms to detect transactional contract violations and ensure consistency.

> [!NOTE] Comment
> - [ ] Wie/wo genau stellt man denn ein, ob man die normale LUW oder die controlled LUW haben will? Oder muss man dazu `CL_ABAP_TX=>modify()` and `CL_ABAP_TX=>save()`  verwenden?


**Key Features:**
- Defines which ABAP statements are allowed/forbidden in specific transactional phases
- Detects violations that result in runtime errors or logging
- Makes applications more robust and the SAP LUW more tangible

**Transactional Phases:**
- Modify phase - includes RAP interaction and early save phases
- Save phase - includes RAP late save phase

Phases can be activated explicitly using `CL_ABAP_TX=>modify()` and `CL_ABAP_TX=>save()` methods, or implicitly through newer ABAP concepts like RAP, Background Processing Framework, and RAP Business Events.

**Transactional Contracts:** APIs are classified with interfaces like `IF_ABAP_TX_SAVE`, restricting their usage to appropriate phases. For example, `CL_BCS_MAIL_MESSAGE->send_async()` cannot be called during the modify phase.

**Common Violations:**
- Database modifications in modify phase (only allowed in save phase)
- Calling classified APIs in wrong phases
- Database changes in RAP handler methods without proper phase activation

This controlled approach ensures data consistency by preventing operations when data might be in an inconsistent state.

### Useful Links
- #Article  [Controlled SAP LUW](https://help.sap.com/docs/abap-cloud/abap-concepts/controlled-sap-luw?locale=en-US)
- #Article  [COMMIT WORK in ABAP Documentation](https://help.sap.com/doc/abapdocu_cp_index_htm/CLOUD/en-US/ABAPCOMMIT.html)
- #Article  [Commit Work](https://help.sap.com/doc/abapdocu_753_index_htm/7.53/en-US/abapcommit.htm)