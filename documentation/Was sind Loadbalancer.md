# Installation und Konfiguration des Loadbalancers

## Was sind Loadbalancer?
kommt noch
## Probleme bei der installation des Loadbalancer
* Informiert und recherchiert wie die Installation abläuft
* Probleme bei der Konfiguration von HAProxy als Load Balancer

## Installation des Loadbalancer
* vm erstellt mit:
    * OS: Ubuntu
    * SCSI: Datastore-vm (Speicher) (Load Balancer-1 = 35GB)
    * 2 - Kerne
    * 4GB Ram
    * Netzwerk: vmbr3

### Profil auf dem Load Balancer
* Name: Tobias (ganz normal)
* your server's name: lb-1
* username: init
* pw: 1-8

### SSH Zugang über PuTTY eingerichtet
* kurze Probleme bei der Verknüpfung des SSH Key's in Putty
---
## Installation von HAProxy & KeepaliveD
```
sudo apt install HAProxy / keepalived
sudo apt install libipset13
```
* unter dem Pfad: 
```
/etc/keepalived/keepalived.conf / haproxy/haproxy.conf
```
* Config geändert
* Recherche nach Configs, Probleme mit Configs
* Simon hat richtige Configs bereitgestellt (siehe Github bei Config)
* keepalived aktivieren & starten/stoppen/neustarten: 
```
systemctl enable --now keepalived.service
systemctl start/stop/restart keepalived / haproxy
```

## Cluster erstellen
* die beiden Loadbalancer müssen zusammenarbeiten, wenn einer nicht mehr verfügbar ist (durch updates oder ausfälle)
* standardmäßig: LB 1 ist der active und LB2 ist der passive
    * KeepaliveD als Cluster weil HAProxy das nicht unterstützt
    * (rsync, crontab)
    * siehe Config in Github
    * Haproxy muss auch laufen - Config auch in Github

## Loadbalancer testen
