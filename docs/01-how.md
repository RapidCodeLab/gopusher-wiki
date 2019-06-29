## How It Works


### Application Parts

The GoPusher consists of several parts, each of them working in docker container. There are next containers: 

* nginx  - web server that proxies all http requests to microservices
* mongodb - document-based database server
* certbot - certbot for getting & update ssl certificates for application domains automatically
* webapp - application dashboard
* eventsapp - application for collect events from service workers
* senderapp - application for send push notifications

Another part is js scripts, included ServiceWorker, that should be placed to your sites for push-notification subscribe request. ServiceWorker send to eventsapp all events and subscriber data.

### Workflow