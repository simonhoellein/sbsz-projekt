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

* Firewall-VM zum laufen bringen
    * Der Firewall-VM ein PCI-Device (Netzwerkkarte) zuweisen
    * erstellung 2 neuer Netzwerkbrücken vmbr1(Projekt-Netz) und vmbr4 (WAN, ip und gateway in netz der schule)

* Konfiguration von pfsense
    * DHCP-Server Gateway, DNS-Server

* Erstellen der 4 Docker-VMs
    * Zuweisen von Ressourcen je VM
        * 4 Cores
        * 16 GB RAM
        * Betriebssystem Ubuntu 22.04.1 Server
    * Konfiguration der VM
        * Zuweisen des Subnet, IP, Gateway, Nameserver
        * Anpassen der Volume-Größe
        * Konfiguration des Server-Name, Benutzername, Passwort
        * Aktivieren von SSH
        * Ablegen der SSH-Public-Keys der Projektmitglieder auf VM, um sich mit SSH und nicht mit Passwort zu verbinden
    * Klonen der ersten VM

* Sicherheit-Features
    * Deaktivieren nicht verwendeter Switch-Ports
    * Verteilung der SSH-Public-Keys der Projektmitglieder auf VMs per Ansible und deaktivieren des Passwort-Logins

* Installation und Konfiguration von Docker inkl. Docker Swarm
    * 

* Installation Network File System (NFS)
    * Aufsetzen von 3 VMs
    * Installation und Konfiguration von GlusterFS
    * 
