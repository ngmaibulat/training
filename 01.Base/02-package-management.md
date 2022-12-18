### Package Manager:

```bash
sudo apt update
apt list | grep vim
sudo apt install vim
```

### Update

```bash
sudo apt update
sudo apt upgrade
```

### Disable IPv6

```
echo 'Acquire::ForceIPv4 "true";' >> /etc/apt/apt.conf.d/99force-ipv4
```
