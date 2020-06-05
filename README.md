# ioBroker-LichtUeberwachung

Dieses Script ist eine bearbeitete Version des [Fensterauswertungs-Script](https://github.com/Pittini/iobroker-Fensterauswertung) von Pittini.

V1.0.0
Dieses Script dient dazu eingeschaltene Lichter pro Raum und gesamt zu zählen.

Folgende States werden angelegt:

* AllLightsOff
* LightsOn
* OverviewTable
* RoomsWithLightsOn
* Für jeden Raum "IsOn und RoomLightsOnCount"

Erklärung zu den States in der Spalte Name!

Alle Stati werden via HTML Tabelle ausgegeben.

# Installation:

**WICHTIG!**

Den Geräten müssen Räume und die Funktion "Licht" zugewiesen sein. Das aber nur dem State "on" oder "Power"! Nicht dem ganzen Gerät.

![Function](https://user-images.githubusercontent.com/42468286/83881339-c26eac80-a740-11ea-9d90-cd357c51a4f8.png)

 1. In der Seitenleiste auf "Aufzählung" klicken
 2. **Wichtig** erst die Function erstellen (ganz unten Benutzerdefiniert Gruppe)
 3. Functionname Licht
 
 ![Räume](https://user-images.githubusercontent.com/42468286/83885839-2f854080-a747-11ea-9036-26775487a9f1.png)
 
 4. Auf Räume wechseln
 5. Neue Aufzählung
 6. Benutzerdefinierte Gruppen für jeden Raum in dem die Lichter gezählt werden sollen!
 
 ![Geräte](https://user-images.githubusercontent.com/42468286/83894727-facab680-a751-11ea-9dc8-698178c0d7b9.png)
 
 7. Editieren "öffnen"
 8. Den State "On", "Switch" oder "Power" auswählen 
 9. Per Drag and Drop in den gewünschten Raum ziehen
 
 ![Function zuweisen](https://user-images.githubusercontent.com/42468286/83895391-ec30cf00-a752-11ea-8656-399eecb56077.png)
 
 10. Es wechselt in die Functions-Ansicht. Den State "On", "Switch" oder "Power" auswählen
 11. Per Drag and Drop in die Function "Licht" ziehen
 12. Wieder zurück auf Räume wechseln und das mit allen Lampen die aufgeführt werden sollen wiederholen.
 
 ![Überprüfen](https://user-images.githubusercontent.com/42468286/83897070-5e0a1800-a755-11ea-8456-ef195c77bfbb.png)
 
 13. Unter Objekte -> Statusansicht deaktivieren
 14. Raum vorhanden
 15. Function Licht vorhanden
 
  **WICHTIG** Unter Instanzen den JavaScript-Adapter neustarten. Script aus dem Code-Teil von Github kopieren.
  
![Skript einfügen](https://user-images.githubusercontent.com/42468286/83898644-7c711300-a757-11ea-89f7-c6c07fd599ce.png)  
  
 16. ioBroker -> Skripte
 17. Unter common ein neues Script anlegen
 18. JavaScript auswählen
 
Code einfügen und speichern nicht vergessen! Skript starten.
 
OverviewTable: Dynamisch erzeugte HTML Tabelle mit allen Räumen und den jeweiligen Lichtstatus. 
Verwendung in Vis als Binding: {javascript.0.LichtUeberwachung.OverviewTable} in einem HTML Widget, optimale Breite 310px, Hintergrundfarbe, Schriftfarbe und Schriftart nach Wahl.

![OverviewTable](https://user-images.githubusercontent.com/42468286/83899458-c9091e00-a758-11ea-8222-e23773f59fe3.png)

Viel Spaß damit!
