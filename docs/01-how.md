## How It Works

### Application Parts

The GoPusher app consists of several parts, each of them working in a Docker container. These are the various containers:

* **nginx** - web server that proxies all http requests to microservices
* **mongodb** - document-based database server
* **certbot** - certbot for getting & update SSL certificates for application domains automatically
* **webapp** - application dashboard
* **eventsapp** - application for collecting events from service workers
* **senderapp** - application for sending push notifications

* **apiapp**  - publishers api (optional)

Another part is all of the scripts, including ServiceWorker, which should be placed on your sites for push-notification subscriber requests. ServiceWorker sends all events and subscriber data to eventsapp.
