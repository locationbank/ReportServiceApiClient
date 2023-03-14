# ReportServiceApiClient
Sections

1. Base API Url
2. Facebook Analytics
3. GMB Analytics
4. Yelp Analytics
5. GmbMedia Analytics
6. Post


# 1 Base API Url

All endpoints described in this document with the exception of Reporting have the following base API url:
https://api.locationbank.net/reportsvc/
# 2 Facebook Analytics

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/Facebook  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
       "clientID": "GUID:cc26d41d-b621-4963-a165-55d8b15a8329",
        "locationID": "",
        "locationName": "Nando's Wimbledon",
        "recordDate": "2020-05-01T00:00:00",
        "latitude": 0,
        "longitude": 0,
        "locality": "",
        "storeCode": "",
        "subLocality": "",
        "country": "",
        "administrativeArea": "",
        "discoverySearches": 542,
        "totalViews": 55,
        "totalActions": 0,
        "totalSearches": 0,
        "websiteActions": 0,
        "directionsAction": 0,
        "phoneCallActions": 0,
        "pagePlaceCheckInTotal": 0,
        "pageNegativeFeedback": 0,
        "directSearches": 0,
        "directionsActions": 0,
        "likesTotal": 7845,
        "likesAdd": 12
    }]
```
 
 
# 3 GMB Analytics 

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/Google  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
      "clientID": "GUID:000000b00-0000-0000-8663-000000002d2b",
        "locationID": "",
        "locationName": "",
        "recordDate": "0001-01-01T00:00:00",
        "subLocality": "",
        "storeCode": "",
        "locality": "",
        "country": "",
        "administrativeArea": "Ireland",
        "latitude": 0,
        "longitude": 0,
        "directSearches": 107246,
        "directionsAction": 4290,
        "discoverySearches": 132259,
        "mapsViews": 482510,
        "phoneCallActions": 4138,
        "searchViews": 124168,
        "totalActions": 12778,
        "websiteActions": 4350,
        "totalSearches": 350299,
        "totalViews": 606678,
        "brandedSearches": 110794,
        "searchQueriesCount": 814,
        "mapsMobileViews": 59,
        "conversationActions": 0,
        "businessBookingsActions": 0,
        "searchDesktopViews": 569,
        "searchMobileViews": 2154,
        "mapsDesktopViews": 25,
        "foodOrderActions": 0,
        "foodMenuClicksActions": 0
    }]
```    

# 4 Yelp Analytics

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/Yelp  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
        "clientID": "GUID:000000b00-0000-0000-8663-000000002d2b",
        "locationID": "",
        "locationName": "",
        "recordDate": "0001-01-01T00:00:00",
        "country": "",
        "administrativeArea": "England",
        "locality": "",
        "storeCode": "",
        "subLocality": "",
        "latitude": 0,
        "longitude": 0,
        "totalViews": 722,
        "totalActions": 49,
        "websiteActions": 19,
        "directionsAction": 22,
        "phoneCallActions": 8
    }]
```    

# 5 GMB media Analytics

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/GmbMedia  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
        "clientID": "GUID:000000b00-0000-0000-8663-000000002d2b",
        "locationID": "",
        "gmbName": "",
        "mediaName": null,
        "createTime": "0001-01-01T00:00:00",
        "isCustomer": false,
        "isDeleted": false,
        "country": "",
        "locationName": "",
        "locality": "",
        "subLocality": "",
        "administrativeArea": "Wales",
        "viewCount": 555642775,
        "viewCountCustomer": 490704768,
        "viewCountMedia": 64938007
    }]
```    


# 6 Post

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Post  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
                  Report types are case sensitive - required)
    FromDate: 2020-07-01T00:00:00 (DateTime - required)
    ToDate: 2020-09-29T23:59:59 (DateTime - required)
    CapaignID: (string[] - at least one capaign must be selected - required)

**Response Json Body**

```json
[{
    "RecordDate": "2020-07-04",
    "ClientId": "GUID:000000b00-0000-0000-8663-000000002d2b",
    "FBNegativeFeedback": "0",
    "GmbNegativeFeedback": "0",
    "FBViewsSearchTotal": "0",
    "GmbViewsSearchTotal": "0",
    "FBViewsTotal": "1961",
    "GmbViewsTotal": "0",
    "FBCallToActionTotal": "22",
    "GmbCallToActionTotal": "0",
    "FBLikes": "10",
    "GmbLikes": "0",
    "FBHahaReactions": "0",
    "FBHideAllposts": "0",
    "FBOtherclicks": "0",
    "FBTotalReactions": "10",
    "FBVideoOtherclicks": "0",
    "FBSadReactions": "0",
    "FBHidePost": "0",
    "FBUnlikePage": "0",
    "FBReportAsSpam": "0",
    "FBLikeReactions": "10",
    "FBVideoLinkclicks": "0",
    "FBWowReactions": "0",
    "FBTotalNegativeFeedback": "0",
    "FBLinkclicks": "0",
    "FBVideoClicksToPlay": "0",
    "FBVideoTotal3SecondViews": "0",
    "FBTotalUniqueImpressions": "0",
    "FBTotalclicks": "0",
    "FBPhotoclicks": "0",
    "FBAngerReactions": "0",
    "FBLoveReactions": "0"
    }]
```    
