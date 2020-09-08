### GET /app/
- Description: List all apps
- Response:
    - 200: 
      ```
           [{name       : 'App name',
             id         : 'app ID',
             url        : 'URL to icon',
             price      : 'price in USD',
             categories : [{name:"category name", subcategory:"subcategory name"}, ...],
             group      : 'Freeware/Shareware'}, ...]
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/app
