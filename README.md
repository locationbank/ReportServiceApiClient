# ReportServiceApiClient
Sections

1. Base API Url
2. Facebook Analytics
3. GBP Analytics
4. GBP Search Keywords
5. Post


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
        "clientID": "GUID:000000b00-0000-0000-8663-000000002d2b",
        "locationID": "",
        "locationName": "",
        "recordDate": "0001-01-01T00:00:00",
        "latitude": 0,
        "longitude": 0,
        "locality": "",
        "storeCode": "",
        "subLocality": "",
        "country": "",
        "administrativeArea": "England",
        "discoverySearches": 401729,
        "totalViews": 147814,
        "totalActions": 225,
        "totalSearches": 0,
        "websiteActions": 29,
        "directionsAction": 13,
        "phoneCallActions": 0,
        "pagePlaceCheckInTotal": 8096,
        "pageNegativeFeedback": 132
    }]
```
 
 
# 3 GBP Analytics 

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
        "searchQueriesCount": 485,
        "searchKeywordNo": 30,
        "value": 485,
        "threshold": 210,
        "searchKeyword": "",
        "locationId": "00000000-0000-0000-0000-000000000000",
        "clientId": "67b9c5e4-6ddf-4856-b3c0-cf27cfe53255",
        "recordDate": "2024-04-01T00:00:00",
        "storeCode": "",
        "locationName": "Nando's Ulundi",
        "administrativeArea": "",
        "subLocality": "",
        "locality": "",
        "country": "",
        "latitude": 0.0,
        "longitude": 0.0,
        "totalSearches": 347,
        "directSearches": 0,
        "discoverySearches": 0,
        "brandedSearches": 0,
        "totalViews": 1003,
        "searchViews": 347,
        "searchDesktopViews": 55,
        "searchMobileViews": 292,
        "mapsViews": 656,
        "mapsDesktopViews": 23,
        "mapsMobileViews": 633,
        "totalActions": 345,
        "websiteActions": 16,
        "directionsActions": 71,
        "phoneCallActions": 253,
        "conversationActions": 0,
        "businessBookingsActions": 0,
        "foodOrderActions": 0,
        "foodMenuClicksActions": 5,
        "id": "00000000-0000-0000-0000-000000000000",
        "version": 0,
        "created": "0001-01-01T00:00:00",
        "modified": "0001-01-01T00:00:00",
        "isDeleted": false
    }]
```

# 4 GBP Search Keywords 

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/Google  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - "SearchKeyword"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[ {
    "clientID": "",
    "locationID": "",
    "locationName": "",
    "recordDate": "2024-09-01T00:00:00",
    "subLocality": "",
    "storeCode": "",
    "locality": "",
    "country": "",
    "administrativeArea": "",
    "latitude": 0,
    "longitude": 0,
    "directSearches": 0,
    "directionsActions": 0,
    "discoverySearches": 0,
    "mapsViews": 0,
    "phoneCallActions": 0,
    "searchViews": 0,
    "totalActions": 0,
    "websiteActions": 0,
    "totalSearches": 0,
    "totalViews": 0,
    "brandedSearches": 0,
    "value": 0,
    "threshold": 0,
    "searchQueriesCount": 236618,
    "mapsMobileViews": 0,
    "conversationActions": 0,
    "businessBookingsActions": 0,
    "searchDesktopViews": 0,
    "searchMobileViews": 0,
    "mapsDesktopViews": 0,
    "foodOrderActions": 0,
    "foodMenuClicksActions": 0,
    "searchKeywordNo": 0,
    "searchKeyword": "nandos"
  }]
``` 

# 5 Post

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
