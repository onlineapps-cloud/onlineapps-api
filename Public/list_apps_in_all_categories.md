### GET /app/category/
* Description: List all apps in all categories
* Response:
    * 200: 
      ```
           [category: [{name:'App name',
                        id:'app ID',
                        url:'URL to icon',
                        price:'price in USD',
                        categories:[{name:"category name", subcategory:"subcategory name"}, ...],
                        lisence:'freeware or shareware'}, ...], ...]
    * 404: **NOT_FOUND**
* Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/app/category/
