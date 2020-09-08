### GET /server/app/{{uid}} 
- Description: List all apps created by a user
- Auth: Bearer key
- Response:
    - 200:   
      ```
           [{name       : 'App name',
             id         : 'app ID',
             url        : 'URL to icon',
             price      : 'price in USD',
             categories : [{name:"category name", subcategory:"subcategory name"}, ...],
             group      : 'Freeware/Shareware',
             servers    : ["ip", "ip", ...]}, ...]
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/server/app/2 \
    --header 'authorization: Bearer {{token}}'
