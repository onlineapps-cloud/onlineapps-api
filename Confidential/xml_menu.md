### GET /xml/menu/{{uid}} 
* Description: Return menu.xml
* Auth: Bearer key
* Response:
    * 200: menu.xml
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL: 
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/xml/menu/2 \
    --header 'authorization: Bearer {{token}}'
  
