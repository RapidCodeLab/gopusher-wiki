# Installation

* [Server Requirments](#server-requirments)
* [Preparing VAPID Key Pair](#preparing-vapid-key-pair)
* [Preparing Domain](#preparing-domain)
* [Preparing Server](#preparing-server)
* [Platform installation](#platform-installation)


## Server Requirments

The minimum hardware requirement is VPS with 2 cores, 2 GB RAM and 40GB SSD. Platform utilize all cores, and for big databases more than 1M subscribers we strongly recommend minimums 4 cores & 4-8GB RAM. We use [MVPS.NET](https://www.mvps.net/?aff=5114){:target="_blank"}, they are fast, cheap and usable.

## Preparing VAPID Key Pair

Go to [VAPID Key Pair Generation Tool](https://vapid-keys.rapidcodelab.repl.run/){:target="_blank"} , enter your email and press ENTER. Don't forget to write down your keys. This data will be used by follow steps.


## Get License Key

Get license key at [License Server](https://lc.rapidcodelab.com/){:target="_blank"}. Don't forget to write down your keys. This data will be used by follow steps.

## Preparing Domain 

To DNS records of domain you chosen for platform working, you should add few records, for the sample: 

    Record: A, Subdomain: web.yourdomain.com , IP: 195.12.34.56 
    Racord: A, Subdomain: events.yourdomain.com , IP: 195.12.34.56
    Racord: AAAA, Subdomain: events.yourdomain.com , IP: 2001:0db8:85a3:0000:0000:8a2e:0370:7334


Instead "web", "events" you can choose anything you think more usable. In this sample "web" is for platform's web application, "events" is for tracking events application. Record AAAA is required if you wanna not miss IPv6 surfers.

## Preparing Server

Software requirements for server: Docker CE, Docker Compose and Git, thats all, install them.

Login to our private docker registry on gitlab with deploy token(read only mode):

```bash 
docker login -u gitlab+deploy-token-73861 -p FGmBV5PLDzvX6aBwa7Lq registry.gitlab.com 
```



## Platform Installation

### Clone deploy repository from github:

```bash
git clone https://github.com/RapidCodeLab/gopusher-public.git
```

### Change files & configs

#### Nginx configuration: /data/app.conf

Change the 'server_name' options depends on domain names you setup earlier. There are two subdomain for eventsapp and webapp containers.

#### Init script: initapp.sh

Init script will automaticly get ssl sertificated for your subdomains and run containers for the first time. Set option 'domains=()' with your data. Don't forget make this file executable with command 'chmod +x initapp.sh' if needed.


#### Docker-compose configuration: docker-compose.yml

Set your license key, VAPID keys, and login&password for admin dashboard.

### Run init script

```bash
./initapp.sh
```

### Login to admin dashboard 

Go to https://your_webapp_domain_or_subdomain.com/panel/dashboard and enter your webapp login&pass.



