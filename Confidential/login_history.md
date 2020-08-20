### GET /history/{{uid}}
* Description: List all IPs, and locations where user logged in
* Auth: Bearer key
* Response:
    * 200: 
      ```
           [{Username    : 'Username',
             Computer    : 'Computer name',
             IP          : 'Client`s IP address ',
             CountryCode : 'Two letter country code (MD)',
             Country     : 'Full country name',
             Time        : 'Login time as yyyy-MM-ddTHH:mm:ss.fffZ"}, ...]
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/history/3 \
    --header 'authorization: Bearer {{token}}'
