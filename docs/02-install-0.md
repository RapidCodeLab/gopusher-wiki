# Server preparing

 This if step by step instruction to prepare server
 before you make gopusher installation. This 
 instruction made for Debian 9 64bit OS.

### Update your system

```bash
apt update

apt upgrade
```

### Install Git
```bash
apt install git
```
### Install Docker-CE
```bash
apt install apt-transport-https ca-certificates curl software-properties-common gnupg2

curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add

add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"

apt update

apt install docker-ce
```
### Install DockerCompose
```bash
curl -L "https://github.com/docker/compose/releases/download/1.24.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose
```