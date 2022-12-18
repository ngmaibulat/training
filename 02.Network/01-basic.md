### Basics

Configuration can be done by using tools like
ip addr, ip route, etc.

However, those settings would not survive reboot. So, you could use startup scripts for those settings.

However, if you want to update settings, it is better to do that in configuration file. Instead of editing the script source.

Also, there are some complexity added by on-demand connections, wifi, VPN, etc. So, in addition to preserving configs accross reboots, you would want system to manage those dynamic events like WiFi, VPN connection, authentication via 802.1X and so on.

To manage all of those things, Linux distro maintainers, created various services/daemons. Currently, two of them are being most popular:

- NetworkD
- SystemD-NetworkD

Ubuntu systems use SystemD-NetworkD.

Also, Canonical created tool called netplan, so it can abstract the configuration from those tools. So, the configuration can stay same, regardless of network management service used. Only the `renderer` option might need to be changed.

### Getting info

```bash
ip addr
ip route
cat /etc/resolv.conf
host google.com
host internal-server
```

### SystemD-NetworkD

```bash
sudo systemctl status systemd-networkd
```
