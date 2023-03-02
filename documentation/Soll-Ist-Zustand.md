# Soll-Ist-Zustand

## Ist-Zustand

**Problemstellung:** Die Gerhard GmbH hostet ihren Online-Shop auf ihren internen Servern. Aufgrund veralteter Hardware fällt die Website regelmäßig aus die IT-Abteilung benötigt durchschnittlich eine 1h bis die Website wieder online ist. In diesem Zeitraum ist der Shop für Kunden nicht erreichbar, was zu hohen Umsatzverlusten führt. Um in Zukunft die Einbußen gering zu halten möchte die Gerhardt GmbH ihren Online-Shop auf extra dafür eingekaufter IT-Hardware hosten.

Der Hersteller HP stellt dem Unternehmen zu Testzwecken folgende Hardware zur Verfügung:

* HP HPE ProLiant DL380 G7 Server (unkonfiguriert)
    * CPU:
    * RAM:
    * Storage:

* HP ProCurve-Switch 2510G-48 Switch (unkonfiguriert)

Zur Konfiguration der Komponenten werden bereits vorhandene Firmengeräte verwendet.

## Soll-Zustand
Die bereitgestellte Hardware wird, entkoppelt von der bestehenden IT-Infrastruktur, installiert und konfiguriert. Zur vereinfachten Administration sollen die bereitgestellten Dienste über Docker Swarm laufen. Zur Darstellung der Website soll ein Webserver mit Wordpress als CMS mit einer Backend-Datenbank implementiert werden. Um die Verfügbarkeit des Servers zu maximieren muss neben einer Redundanz aller kritischer Ressourcen auch der Schutz vor Angriffen berücksichtigt werden. Zudem sollen die Systemressourcen skalierbar sein, dass der Server auch bei steigenden Besucherzahlen über ausreichend Leistung verfügt.

Test123