# API Documentation for OnlineApps

All requests relative to https://requests.onlineapps.cloud

* Post request body is `application/x-www-formurlencoded`
* Auth token is passed as `Authorization: "Bearer {{token}}"` header, see [Confidential/login.md](https://github.com/onlineapps-cloud/onlineapps-api/blob/master/Confidential/login.md) to get token
* When `{{}}` is used, it is a placeholder (Most often for uid/token)
