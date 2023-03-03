# Keepalived

## Install:
```
sudo apt update
sudo apt install keepalived
sudo apt install libipset13
```

## Config:
* guck doch einach in den config files nach ;)
* Pfad: `/etc/keepalived/keepalived.conf`

keepalived aktivieren:
```
systemctl enable --now keepalived.service
```