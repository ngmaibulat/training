### Basic Info:

```bash
uname
uptime
lsb_release -a

ip addr
ip addr | grep inet
cat /etc/resolv.conf
ls -la
pwd
df -h

apt list | grep installed
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

### Hostname

```bash
cat /etc/hostname
hostname
hostname -d
hostname -f

sudo hostnamectl hostname dev
```
