# ReportServiceApiClient
Sections

1. Base API Url
2. Facebook Analytics
3. GBP Analytics
4. GBP Search Keywords
5. Post
6. Bing Analytics
7. Apple Analytics
8. Store Locator Location Page Analytics
9. Store Locator Main Page Analytics


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
# 6 Bing Analytics 

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/Bing  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
        "locationId": "1ba69757-f901-4bfb-956f-cc40103c5f80",
        "clientId": "67b9c5e4-6ddf-4856-b3c0-cf27cfe53255",
        "recordDate": "2024-10-01T00:00:00",
        "storeCode": "",
        "locationName": "Nando's Grassy Park Drive Thru",
        "administrativeArea": "",
        "subLocality": "",
        "locality": "",
        "country": "",
        "latitude": 0,
        "longitude": 0,
        "bingTotalImpressions": 4,
        "bingSearchImpressions": 4,
        "bingSearchDesktop": 0,
        "bingSearchMobile": 4,
        "bingMapsImpressions": 0,
        "bingMapsDesktop": 0,
        "bingMapsMobile": 0,
        "bingTotalClicks": 0,
        "bingCalls": 0,
        "bingCallsSearchDesktop": 0,
        "bingCallsSearchMobile": 0,
        "bingCallsMapsDesktop": 0,
        "bingCallsMapsMobile": 0,
        "bingDirections": 0,
        "bingDirectionsSearchDesktop": 0,
        "bingDirectionsSearchMobile": 0,
        "bingDirectionsMapsDesktop": 0,
        "bingDirectionsMapsMobile": 0,
        "bingWebsite": 0,
        "bingWebsiteSearchDesktop": 0,
        "bingWebsiteSearchMobile": 0,
        "bingWebsiteMapsDesktop": 0,
        "bingWebsiteMapsMobile": 0,
        "bingFoodMenu": 0,
        "bingFoodMenuSearchDesktop": 0,
        "bingFoodMenuSearchMobile": 0,
        "bingFoodMenuMapsDesktop": 0,
        "bingFoodMenuMapsMobile": 0,
        "bingOrderOnline": 0,
        "bingOrderOnlineSearchDesktop": 0,
        "bingOrderOnlineSearchMobile": 0,
        "bingOrderOnlineMapsDesktop": 0,
        "bingOrderOnlineMapsMobile": 0
    }]
```
# 7 Apple Analytics 

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/Apple  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData", "DailySeries"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
      "AppleLocationId": "00000000-0000-0000-0000-000000000000",
      "AppleClientId": "00000000-0000-0000-0000-000000000000",
      "AppleRecordDate": "0001-01-01T00:00:00Z",
      "AppleStoreCode": "",
      "AppleLocationName": "",
      "AppleAdministrativeArea": "",
      "AppleSubLocality": "",
      "AppleLocality": "",
      "AppleCountry": "",
      "AppleLatitude": 0.0,
      "AppleLongitude": 0.0,
      "AppleSearchTapsTotal": 0,
      "AppleSearchTaps": 0,
      "AppleSearchNameTaps": 0,
      "AppleSearchCategoryTaps": 0,
      "AppleSearchOtherTaps": 0,
      "AppleSpatialSearchTaps": 0,
      "AppleSpatialDirectionTaps": 0,
      "ApplePlaceCardTotalClicks": 0,
      "ApplePlaceCardJoinWaitlist": 0,
      "ApplePlaceCardOrderDelivery": 0,
      "ApplePlaceCardOrderFood": 0,
      "ApplePlaceCardOrderTakeout": 0,
      "ApplePlaceCardPickup": 0,
      "ApplePlaceCardReserveParking": 0,
      "ApplePlaceCardReserveTable": 0,
      "ApplePlaceCardScheduleAppointment": 0,
      "ApplePlaceCard": 0,
      "ApplePlaceCardCallTaps": 0,
      "ApplePlaceCardDirectionTaps": 0,
      "ApplePlaceCardOrderTaps": 0,
      "ApplePlaceCardShareTaps": 0,
      "ApplePlaceCardShowcaseTaps": 0,
      "ApplePlaceCardWebsiteTaps": 0,
      "ApplePlaceCardViews": 0,
      "ApplePlaceCardViewAvailability": 0,
      "ApplePlaceCardMenuViews": 0,
      "ApplePlaceCardViewPricing": 0,
      "ApplePlaceCardGalleryEngagement": 0,
      "ApplePlaceCardTapBuyTickets": 0,
      "AppleTotalLocationSearchTaps": 0,
      "AppleTotalPlaceCardClicks": 0,
      "AppleTotalSpecialLocationSearch": 0
    }]
```

# 8 Store Locator Location Page Analytics 

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/StoreLocator/LocationPage  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
        "slLocationId": "00000000-0000-0000-0000-000000000000",
        "slClientId": "67b9c5e4-6ddf-4856-b3c0-cf27cfe53255",
        "slRecordDate": "0001-01-01T00:00:00+00:00",
        "slStoreCode": "",
        "slLocationName": "",
        "slAdministrativeArea": "",
        "slSubLocality": "",
        "slLocality": "",
        "slCountry": "ZA",
        "slCustomType": "delivery",
        "slContext": null,
        "slDirectionsActions": 0,
        "slPhoneCallActions": 0,
        "slPostActions": 0,
        "slMediaActions": 0,
        "slSocialProfileActions": 0,
        "slReviewActions": 0,
        "slFirstPartyReviewActions": 0,
        "slView": 0,
        "slCustomActions": 298
    }]
``` 
# 9 Store Locator Main Page Analytics

* Http Verb: GET
* Headers: Content-Type: application/json
* Http EndPoint: /Analytics/StoreLocator/MainPage  https://api.locationbank.net/reportsvc/

**QueryString Parameters:**

    ClientID: (string - Unique client id for every client - required)
    ReportType: (string - Supported report types are "Location", "SubLocality", "Locality", "AdministrativeArea", "Country", "MonthlyData"
                  Report types are case sensitive - required)
    FromDate: 2020-09-01T17:16:40 (DateTime - required)
    ToDate: 2020-09-29T17:16:40 (DateTime - required)

**Response Json Body**

```json
[{
        "slLocationId": "00000000-0000-0000-0000-000000000000",
        "slClientId": "67b9c5e4-6ddf-4856-b3c0-cf27cfe53255",
        "slRecordDate": "0001-01-01T00:00:00+00:00",
        "slStoreCode": "",
        "slLocationName": "",
        "slAdministrativeArea": "",
        "slSubLocality": "",
        "slLocality": "",
        "slCountry": "ZA",
        "slCustomType": "",
        "slContext": null,
        "slDirectionsActions": 0,
        "slPhoneCallActions": 0,
        "slPostActions": 0,
        "slMediaActions": 0,
        "slSocialProfileActions": 0,
        "slReviewActions": 0,
        "slFirstPartyReviewActions": 0,
        "slView": 578,
        "slCustomActions": 0
    }]
```

