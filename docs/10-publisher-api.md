## Publishers API


### How to enable Publishers API

To enable publishers api, uncomment the corresponding lines in files  docker-compose.yml and /data/nginx/app.conf, then restart services.


### API Authorization

For making your api requests authorized, add two HTTP headers to each request with names APIKey, APIEmail that contains your actual data.


### API Endpoints

* GET */api/getSubscribers* - returns amount of total subscribed, unique subscribed and unsubscribed users by day. By default returns data for current month. You can use  a few GET params to filter returned data: 
    * *countries* - to filters data by country. For example: ?countries=RU,UK,US
    * *channels* - to filter data by channels. For example: ?countries=default,entertainment,chan_1
    * *from* & *to* - to filter data by dates. For example: ?from=09/01/2019&to=09/30/2019


* GET */api/getPayments* - returns payments that was made to publisher.
* GET */api/getBalance* - return publisher's balance.
* GET */api/getCountries* - returns available countries to use in filter of method /api/getSubscribers
* GET */api/getChannels* - returns available channels to use in filter of method /api/getSubscribers