﻿# db_project
Eine Rest API, die den Gleisabschnitt ausgibt, wenn man die Zugnummer, die Wagennummer und die Bezeichnung (Ril100) des Bahnhofes übergibt. 

## Beschreibung der Lösung
Die Schnittstelle /station nimmt 3 Parameter entgegen, den int "myTrainNumber", die Zugnummer, den int "myWaggon" und den String "ril100", das Kürzel des Bahnhofes. Als Ausgabe bekommt man alle Gleisabschnitte, an denen der Zug mit der übergebenen Nummer und die Zugabschnitte mit der übergebenen Wagennummer halten und den dazugehörigen Gleisabschnitten. Der Gleisabschnitt wird mit ausgegeben, da Zugnummern unter mehreren Gleisen aufgeführt sein können. Als Datenquelle gibt es xml-Dateien, die verschiedene Infos zum Bahnhof enthalten. Über die API wird zuerst die passende xml-Datei aus dem Ordner gesucht und in ein Java-Object gemapped.

## Frameworks
Für die Erstellung der Rest-API wurde das Framework Spring Boot benutzt. Des Weiteren wurde das Jackson Databind Framework für das Mapping der XML benutzt und für die "Ignore-Properties"-Funktion. Da die xml-Datei sehr komplex ist und nicht jedes Attribut daraus gebraucht wird, wurden nicht erstellte Attribute ignoriert. Die Frameworks wurden über Maven eingebunden und heruntergeladen.
