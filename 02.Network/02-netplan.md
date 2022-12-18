### Netplan

```bash
ls /etc/netplan/*.yaml
sudo netplan try
sudo netplan apply

ip addr | grep inet
ip route
```

```yaml
network:
  ethernets:
    ens33:
      dhcp4: false
      link-local: []
      addresses: [192.168.35.132/24]
      nameservers:
        search: [domain.local, ext.com]
        addresses: [8.8.8.8, 1.1.1.1]
      routes:
        - to: default
          via: 192.168.35.2
        - to: 10.10.10.0/24
          via: 192.168.35.100
  version: 2
```

### Docs

- https://netplan.io/examples
- https://github.com/canonical/netplan
- https://netplan.io/design
- https://netplan.io/reference
