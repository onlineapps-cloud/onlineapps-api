### GET /associations/{{uid}}
- Description: List Apps associated to certain extensions
- Auth: Bearer key
- Response:
    - 200: 
      ```
           [{"extension":extension,
             "options":[{"id"        : app ID
                         "appName"   : app name,
                         "hasIcon"   : true/false,
                         "IsSelected": true/false},...]
             },...]
      ```
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/associations/2 \
    --header 'authorization: Bearer {{token}}'
