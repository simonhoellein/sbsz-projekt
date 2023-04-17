# Netzwerk Dokumentation - internal

## IPs

|IPs|Description|A-Record|
|---|-----------|--------|
|1  |pfsense    |gw-1    |
|5  |switch     |sw-1    |
|10 |proxmox    |prox-1  |
|15 |ilo        |ilo     |
|20 |haproxy-vip|lb-vip  |
|21 |haproxy-1  |lb-1    |
|22 |haproxy-2  |lb-1    |
|41 |docker-1   |docker-1|
|42 |docker-2   |docker-2|
|43 |docker-3   |docker-3|
|44 |docker-4   |docker-4|
|45 |docker-5   |docker-5|
|100|start-dhcp |--------|
|200|end-dhcp   |--------|

## HOWTO - Connect via ssh

1. keypair mit `ssh-keygen -b 4096` erzeugen
2. ssh public-key (`id_rsa.pub`) in Keystore vom root-user auf VM importieren (`/root/.ssh/authorized_keys`)
3. mit `ssh root@<ip>` verbinden, key `id_rsa` wird automatisch genutzt solange er im `.ssh` Verzeichnis des users ist