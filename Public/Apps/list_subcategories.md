### GET /category/<category>
**MAY BE SOON DEPRECATED**
- Description: List all subcategories in a category
- Response: 
    - 200: `['subcategory', ...]`
    - 404: **NOT_FOUND**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/category/2D%20Graphics
