# Installation

* [Server Requirments](#server-requirments)
* [Preparing VAPID Key Pair](#preparing-vapid-key-pair)
* [Preparing Domain](#preparing-domain)
* [Preparing Server](#preparing-server)
* [Platform installation](#platform-installation)


## Server Requirments

The minimum hardware requirement is a VPS with 2 cores, 2 GB RAM, and 40GB SSD. The platform utilizes all cores, and for big databases with more than 1 Million subscribers we strongly recommend a minimum of 4 cores and 4-8GB RAM. We use [MVPS.NET](https://www.mvps.net/?aff=5114){:target="_blank"}, they are fast, cheap, and usable.

## Preparing VAPID Key Pair

Go to the [VAPID Key Pair Generation Tool](https://vapid-keys.rapidcodelab.repl.run/){:target="_blank"}, enter your email, and press ENTER. Don’t forget to write down your keys. This data will be used in the following steps.


## Get License Key

Get a license key at the [License Server](https://lc.rapidcodelab.com/){:target="_blank"}. Don’t forget to write down your keys. This data will be used by following steps.


## Preparing Domain 

Log into your domain control panel and based on the example down below, add the following DNS records:

    Record: A, Subdomain: web.yourdomain.com , IP: your server ipv4 
    Racord: A, Subdomain: events.yourdomain.com , IP:  your server ipv4 
    Racord: AAAA, Subdomain: events.yourdomain.com , IP:  your server ipv6

Instead “web”, “events” you can choose anything you think more usable. In this example, “web” is for platform’s web application, “events” is for tracking events application. Record AAAA is required if you don’t want to miss IPv6 surfers.


## Preparing Server

Software requirements for the server are: Docker CE, Docker Compose, and Git. That’s all, simply install those three pieces of software.

Login to our private docker registry on gitlab with deploy token (read only mode):

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

Change the ‘server_name’ options depending on the domain names you setup earlier. There are two subdomains for the eventsapp and webapp containers.

#### Init script: initapp.sh

Init script will automatically get SSL certified for your subdomains and run containers for the first time. Set up option ‘domains=()’ with your data. Don’t forget to make this file executable with the command ‘chmod +x initapp.sh’ if needed.


#### Docker-compose configuration: docker-compose.yml

Set your license key, VAPID keys, login and password for the admin dashboard.

### Run init script

```bash
./initapp.sh
```

### Login to admin dashboard 

Go to https://your_webapp_domain_or_subdomain.com/panel/dashboard and enter your webapp login and password.

