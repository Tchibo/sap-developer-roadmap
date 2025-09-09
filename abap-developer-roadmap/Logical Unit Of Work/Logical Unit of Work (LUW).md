
> [!NOTE] Title
> - [ ] #Basic oder #Intermediate ?
> - [ ] Wie startet man eine LUW? Wie beendet man sie?
> - [ ] COMMIT und ROLLBACK erwähnen?
> - [ ] Kannst du ein Beispiel geben? ...Ich habe eine SalesOrder und ein SalesOrderItem. Wenn die SalesOrder nicht gespeichert werden kann, soll das Item auch nicht gesichert werden. Sowas in der Art.
> - [ ] Anscheinend gibt es einen Unterschied zwischen der SAP LUW und der Datenbank LUW. -> Vllt. die Info hinzufügen, dass Datenbankänderungen in der SAP LUW zwischengespeichert werden und erst beim Commit zur Datenbank gelangen. Und dass wir die Daten auch aus dem Zwischenspeicher Lesen (ohne bypassing buffer).
> - [ ] Links? Hab diesen Blog Beitrag gefunden, der ist aber nur so mittel gut: https://community.sap.com/t5/application-development-and-automation-blog-posts/what-is-luw-how-luw-works-different-types-of-luw/ba-p/13547262

A Logical Unit of Work (LUW) is one of the most fundamental concepts in SAP for ensuring data consistency. It represents a sequence of logically connected steps that must be executed as an inseparable, atomic unit. The principle is simple: all steps succeed, or no steps succeed. This "all-or-nothing" approach prevents the database from being left in a partial, inconsistent state if an error occurs mid-process.