­­
## Features Overview

### Web Push Notifications using the VAPID method

The application uses the VAPID (Voluntary Application Server Identification) method to send push notifications directly to push services, bypassing FCM (Google Firebase Cloud Messaging). VAPID (Voluntary Application Server Identification) is the newest way to receive and send push notifications on the web.

### Written on Golang, packed to Docker container

Golang is a programming language developed by Google, it provides faster execution applications, light concurrency, etc. Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, including libraries and other dependencies and ship the entire application out as one package. Docker provides an application independent from a specific OS, allowing you to run your application on any unix system without any troubles.

### Unlimited subscribers load

Operate with millions of subscribers on simple VPS, and the application will still be fast.

### Subscriber tracking by channels

Place a subscription code on any sites and separate them by channel for follow targeting. For example, set channels “adult”, “entertainment”, “business”, or even “yoursite.com” and target by these individual channels in different campaigns.

### Entirely self-hosted web application

You have full control over your subscriber database, no one else will have access to it. You control how often to send push notifications, so you can prevent unsubscribe actions that can happen when somebody tries to spam to your subscribers. You can also send push notifications without any type of moderation like in ad networks.

### Buy Web Push Notification subscribers from third parties and set your own rates

Set your own rates by country and buy subscribers from anyone who installs your subscribing code on their sites. Pay them earnings based on the number of subscribers you buy from them.

### Detailed statistics on publishers, sources, geo, and campaigns

Subscriber stats by publisher, channel, country, and date range. Campaign stats show all of the information detailing how many push notifications were sent, delivered, impressed, clicked on, and closed.

### A/B testing for self-run creative sets and external DSPs

Each campaign can send many different creative sets and external DSPs by the assigned weight. That means, for example, you can add two creatives to a campaign and set the weights at 80% for the first creative and 20% for the second creative. This means that in 80% of cases the app will send creative #1, and in the other 20% of cases the app will send creative #2.

### Schedule notifications based on subscriber’s time zones

The scheduler is based on each subscriber’s time zone, so, if you set the notification for 7:00 AM for all countries, each subscriber will receive the push notification once it is 7:00 AM in their time zone.

### Personalized Push Notifications based on geo & device data
In creatives you can use templates ##CITY##, ##REGION##, ##COUNTRY##, ##OS##, ##PLATFORM##, ##BROWSER##, and they will be replaced with actual subscriber data.

### Rich push notifications, Emoji support 👽 👍

Creatives support this push notification data: title, body, icon, image, badge, vibrate, and up to two action buttons. The fields title, body, and action buttons support emojis.

### Rich targeting by geo, device type, platform, browser, browser language

Campaigns have the ability to conduct rich targeting by channels, countries, regions, cities, device types, platforms, browser, and browser language.

### Unlimited number of sources on one platform

One platform can receive subscribers from an unlimited number of sites.

### Supports OpenRTB & OpenRTB Dynamic Native Ads

The application can request ads from external DSP that support OpenRTB & OpenRTB Dynamic Native Ads. For each subscriber in the campaign, the application will request ads with subscriber’s data and send push notifications based on the response. Minimum requirements for DSP is the ability to serve 500 requests/second.