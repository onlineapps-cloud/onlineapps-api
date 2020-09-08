### GET /app/category/
- Description: List all apps in all categories
- Response:
    - 200: 
      ```
           [category: [{name       : 'App name',
                        id         : 'app ID',
                        url        : 'URL to icon',
                        price      : 'price in USD',
                        categories : [{name:"category name", subcategory:"subcategory name"}, ...],
                        group      : 'Freeware/Shareware'}, ...], ...]
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/app/category/
