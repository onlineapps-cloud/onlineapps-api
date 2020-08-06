### GET /category/<category>
* Description: List all subcategories in a category
* Response: 
    * 200: `['subcategory', ...]`
    * 404: **NOT_FOUND**
* Example cURL:
  ```
    curl --request GET \
    --url http://requests.onlineapps.cloud:1880/category/2D%20Graphics
