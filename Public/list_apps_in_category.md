### GET /app/category/<category_or_subcategory>
* Description: List all apps in a category, or a subcategory
* Response:
    * 200: 
      ```
           [{name:'App name',
             id:'app ID',
             url:'URL to icon',
             price:'price in USD',
             categories:[{name:"category name", subcategory:"subcategory name"}, ...],
             lisence:'freeware or shareware'}, ...]
    * 404: **NOT_FOUND**
* Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/app/category/2D%20Editor
