```bash

sudo systemctl status systemd-networkd

cat  /run/systemd/network/10-netplan-ens33.network
```

```ini
[Match]
Name=ens33

[Network]
LinkLocalAddressing=no
Address=192.168.35.132/24
DNS=8.8.8.8
Domains=domain.local other.local ext.com

[Route]
Destination=0.0.0.0/0
Gateway=192.168.35.2

[Route]
Destination=10.10.10.0/24
Gateway=192.168.35.100
```
