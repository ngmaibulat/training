### Tools used:

-   VMware Player/Fusion
-   Visual Studio Code
-   Markdown
-   Hyper (https://hyper.is/)
-   Ubuntu Server 2022
-   https://mailtrap.io
-   https://ray.so

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

### SSH

```bash
ssh-keygen
ssh-copy-id user@host
ssh user@host
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

### VIM Editor

```bash
sudo apt install vim
vim filename.sh
bash filename.sh
```

### Package Manager:

```bash
apt list | grep vim
sudo apt install vim
```

### NodeJS

```bash
sudo apt install nodejs
sudo apt install npm
node -v
npm -v
sudo npm install -g n
sudo npm install -g typescript
```

### Switching NodeJS versions:

```bash
sudo n lts
sudo n latest
bash
node -v
npm -v
sudo n
node -v
npm -v
```

### Swaks

```bash
sudo apt install swaks

swaks -t user@example.com -f me@example.com --auth CRAM-MD5 --auth-user b6b95bd694196a  -tls -s smtp.mailtrap.io:2525

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

### htop

```
sudo apt install htop
htop
```

### Local Test Webserver

```bash
sudo npm install -g serve
serve
```

### PM2

```bash
sudo apt install iputils-ping
sudo npm install -g pm2
sudo pm2 startup
pm2 save

pm2 start 'ping google.com' --name ping
pm2 ls
pm2 logs 0
pm2 delete 0

pm2 save
```

### Update

```bash
sudo apt update
sudo apt upgrade
```

### Sharing Terminal Output

```
sudo apt install netcat
ls -la  | nc seashells.io 1337
htop  | nc seashells.io 1337
```
