# Netzwerk Dokumentation - internal

## IPs

`192.168.0.5`   - sw-1
`192.168.0.10`  - proxmox
`192.168.0.1`   - gw-1

## HOWTO - Connect via ssh

1. keypair mit `ssh-keygen -b 4096` erzeugen
2. ssh public-key (`id_rsa.pub`) in Keystore vom root-user auf VM importieren (`/root/.ssh/autherized_keys`)
3. mit `ssh root@<ip>` verbinden, key `id_rsa` wird automatisch genutzt solange er im `.ssh` Verzeichnis des users ist