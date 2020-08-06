### GET /app/
* Description: List all apps
* Response:
    * 200: 
      ```
           [{name:'App name',
             id:'app ID',
             url:'URL to icon',
             price:'price in USD',
             categories:[{name:"category name", subcategory:"subcategory name"}, ...],
             lisence:'freeware or shareware'}, ...]
* Example cURL:
  ```
    curl --request GET \
    --url http://requests.onlineapps.cloud:1880/app