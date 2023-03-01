# Dokumentation der Installation des Servers

* Substitution von 6 bestehenden 6 von 18 RAM-Riegel durch 16GB-RAM-Riegel ausgetauscht

* Anpassen der Konfigurationen im BIOS (Zeit,...)

* Anschließen an das Schulnetzwerk, um über den Backbone mit privaten Clients auf Server zu verbinden

* Konfiguration des Integrated Lights-Out 3 (ILO)
    * aktivieren von DHCP

* Konfiguration des RAID-Controllers
    * RAID 1 auf 2 HDDs a 300GB
    * RAID 50 auf 6 HDDs a 300GB
    * 2,4TB Gesamtspeicher
    * davon nutzbar 1,8TB exclusive 300GB für Mirror und 300GB für Parity
    * --> RAID 50 wegen Kriterium der hohen Verfügbarkeit

* Installation des Betriebssystems über USB-Stick
    * OS: Proxmox VE 6.4
    * Verbindung über Netzwerk mit privatem Notebook per ILO Integrated Remote Console - Server
    * Konfiguration von Zeitzone, Sprache, Tastaturlayout, Kennwort, Hostname, IP, Gateway, DNS, E-Mail

* Problem: Montior unterstützt Frequenz von Proxmox Installer nicht
    * Lösung: Installation von ILO Integrated Remote Console - Server auf privatem Surface und Verbindung über Schulnetzwerk mit Server
    * Sobald Installation abgeschlossen war änderte sich die Frequenz und der Schulmonitor unterstützte diese wieder 

* Konfiguration im Proxmox Virtual Enviroment
    * Erstellen von Benutzern-Konten für Gruppenmitglieder

* Hochladen der ISO-Dateien
    * Ubuntu-Image für VMs
    * Pfsense Firewall-Image

* Namensgebung der belegten Switch-Ports

* Fehlerbehebung bei PCI-Passtrough
    * Fehlerursache: Gemeinsame Ressourcen des Servers müssen auf VM und Server-Betriebssystem verteilt werden
    * Konfiguration des Kernels

* Einbau Server und Switch in mobiles Cisco-Rack