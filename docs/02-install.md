# Installation

* [Server Requirments](#server-requirments)
* [Preparing Server](#preparing-server)
* [Platform installation](#platform-installation)


## Server Requirments

The minimum hardware requirement is VPS with 2 cores, 2 GB RAM and 40GB SSD. Platform utilize all cores, and for big databases more than 1M subscribers we strongly recommend minimums 4 cores & 4-8GB RAM. We use [MVPS.NET](https://www.mvps.net/?aff=5114), they are fast, cheap and usable.

## Preparing VAPID Key Pair

Go to [VAPID Key Pair Generation Tool](https://vapid-keys.rapidcodelab.repl.run/) , enter your email and press ENTER. Don't forget to write down your keys. This data will be used by follow steps.

## Preparing Server

```bash 
docker login -u gitlab+deploy-token-73861 -p FGmBV5PLDzvX6aBwa7Lq registry.gitlab.com 
```


## Plartform Installation

