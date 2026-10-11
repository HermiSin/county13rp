# Entwicklung

Stand: 11. Oktober 2026.

## Technische Grundlage

County 13 verwendet FiveM/GTA V. Laut aktueller interner Betriebsdokumentation wurde Qbox über txAdmin installiert; oxmysql ist vorhanden. Eine öffentlich versionierte Abhängigkeitsliste und ein reproduzierbarer Entwicklungsserver sind noch auszuarbeiten. Bestehende Versionsnummern oder Schnittstellen dürfen deshalb nicht aus diesem Gerüst abgeleitet werden.

## Lokaler Einstieg

```sh
git clone https://github.com/HermiSin/county13rp.git
cd county13rp
git switch -c feature/kurze-beschreibung
```

Die Dokumente lassen sich unmittelbar lesen und bearbeiten. Das Repository allein startet keinen Spielserver. Für Ressourcenentwicklung ist ein eigener Testserver erforderlich. Produktive Zugänge werden nicht über GitHub geteilt.

## Eigene Ressourcen

Eigene Ressourcen werden in `resources/[county13]/c13_<name>/` abgelegt. Jede Ressource benötigt ein `fxmanifest.lua` und eine README mit Zweck, Abhängigkeiten, Konfiguration und tatsächlich durchgeführten Prüfungen. Abhängigkeiten und Lizenzen werden vor der Aufnahme geprüft; fremde Frameworks und gekaufte Inhalte werden nicht pauschal kopiert.

Geld, Inventaränderungen, Dokumentenzugriff und Berechtigungen werden serverseitig geprüft. Clientdaten gelten nicht als Berechtigungsnachweis. Vertrauliche Inhalte dürfen nicht in Clientskripten oder NUI-Dateien ausgeliefert werden.

## Konfiguration und Betrieb

`config/county13.example.cfg` zeigt nur das Einbinden eigener Ressourcen. Lizenzschlüssel, Datenbankverbindungen und Adminzuordnungen werden außerhalb der Versionskontrolle gepflegt. Das Beispiel ersetzt weder die Qbox-Konfiguration noch die produktive `server.cfg`.

Deployment ist ein eigener, bewusst ausgeführter Schritt. Ein Push in dieses Repository verändert den laufenden Server nicht. Vor einer späteren Deployment-Automatisierung sind ein Teststand, ein Backup und ein Wiederherstellungsverfahren erforderlich.

## Quellen und Wissensgrenzen

`docs/spieler-lore.md` enthält die freigegebene öffentliche Lore. Gerüchte sind keine bestätigten Tatsachen und begründen nicht automatisch Charakterwissen. Interne Konzept- und Lore-Dateien werden getrennt gepflegt und vor relevanten Änderungen vom berechtigten Projektteam gelesen.
