### Basic Info:

```bash
uname
uptime
ip addr
ip addr | grep inet
cat /etc/resolv.conf
ls -la
pwd
df -h
```

### Sudo

```bash
ls /root
sudo ls /root
```

### Working with Directories and Files

```bash
ls -la
pwd
mkdir newdir
cd newdir
touch newfile
echo $USER >> newfile
cat newfile
cd ..
rm -fr newdir
```

### VM Guest Tools

```bash
sudo apt install open-vm-tools
sudo systemctl status open-vm-tools
```

### Reboot/Shutdown

```bash
sudo reboot
sudo halt
```
