### Basics

```bash
cat /etc/resolv.conf

sudo systemctl status systemd-resolved

resolvectl

resolvectl query google.com

resolvectl flush-caches

```

### See per interface settings

```bash
resolvectl domain
```

Output above shows that certain domains should be resolved via certain network interface.
That especially usefull if using VPN to corporate network.

```bash
resolvectl dns
```

Outbput above shows which DNS server is being
used for a particular interface. Hence, you can see that we can have `Split DNS`

### Finding various records:

```
host -t mx google.com

host -t txt google.com | grep spf
host -t txt _spf.google.com

host selector1._domainkey.forcepoint.com
host -t txt selector1-forcepoint-com._domainkey.forcepointcml.onmicrosoft.com.
```

### Resources

- https://fedoramagazine.org/systemd-resolved-introduction-to-split-dns/

- https://manpages.ubuntu.com/manpages/xenial/man8/systemd-resolved.service.8.html

- https://www.freedesktop.org/wiki/Software/systemd/writing-network-configuration-managers

- https://www.freedesktop.org/wiki/Software/systemd/writing-resolver-clients
