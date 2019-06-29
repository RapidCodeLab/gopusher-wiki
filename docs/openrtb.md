### OpenRTB 2.5  & OpenRTB Dynamic Native Ads API Specification Version1.2

#### BidRequest

```json
{
  "id": "129ca6dd-5403-4476-a4a6-555d6a538bc4",
  "user":{
    "id": "129ca6dd-5403-4476-a4a6-555d6a538bc4", 
    "ext":{
      "age":86400 
    }
  },
  "site":{
    "id": "23423", 
    "publisher":{
      "id": "23234" 
    }
  },
  "device":{
    "language": "en",
    "geo":{
      "country": "DE", 
      "city":"Berlin", 
      "region":"Brandenburg" 
    },
    "os":"Android",
    "devicetype":1,
    "ip":"212.23.123.12",
    "ipv6": "",
    "ua":"Mozilla/5.0 (Windows NT 6.3; WOW64; rv:36.0) Gecko/20100101 Firefox/36.0"
  },
  "imp":[{
    "id": "1",
    "bidfloor": 0.12,
    "bidfloorcur": "USD",
    "secure":1,
    "native":{
      "request":"native object serialized",
      "ver":"1.2"
    }
  }],
  "at": 1, 
  "tmax": 500,
  "cur":["USD"]
}
```
#### Native Ad Request

```json
{
  "native":{
    "ver":"1.2",
    "assets":[{
      "id":1,
      "required":1,
      "title":{
        "len":140
      }
    },{
      "id":2,
      "required":1,
      "img":{
        "type":1,
        "wmin":192,
        "hmin":192
      }
    },{
      "id":3,
      "required":0,
      "img":{
        "type":3,
        "wmin":800
      }
    },{
      "id":4,
      "required":1,
      "data":{
        "type":2
      }
    }
    ]
  }
}
```

### BidResponse
```json
{
  "id":"129ca6dd-5403-4476-a4a6-555d6a538bc4",
  "seatbid":[{
    "bid":[{
      "id":"generated id",
      "impid":"1",
      "price":0.02,
      "adm":"native ad response obj"
    }]
  }]
}
```

#### Native Ad Response

```json
{
  "native": {
    "link": {
      "url": "https://adurl.com/"
    },
    "assets": [
      {
        "id": 1,
        "required": 1,
        "title": {
          "text": "Push Notificaion Title"
        }
      },{
        "id": 2,
        "required":1,
        "img":{
          "url":"https://push-notification-icon-url.com/icon.jpg"
        }
      },{
        "id": 3,
        "required":0,
        "img":{
          "url":"https://push-notification-image-url.com/image.jpg"
        }
      },{
        "id":4,
        "required":1,
        "data":{
          "value":"Push notification body"
        }
      }
      
    ]
  }
}
```
