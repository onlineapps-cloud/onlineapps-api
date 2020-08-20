### GET /app/user/{{uid}} 
* Description: List all apps purchased by a user
* Auth: Bearer key
* Response:
    * 200:   
      ```
           [{name       : 'App name',
             id         : 'app ID',
             url        : 'URL to icon',
             price      : 'price in USD',
             categories : [{name:"category name", subcategory:"subcategory name"}, ...],
             lisence    : 'freeware or shareware',
             status     : 'is it frozen or available'}, ...]
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/app/user/2 \
    --header 'authorization: Bearer {{token}}'
