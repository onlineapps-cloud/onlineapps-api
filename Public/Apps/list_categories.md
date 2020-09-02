### GET /category/
- Description: List all categories and theid subcategories 
- Response: 
    - 200: `{'category':['subcategory', ...], ...}` 
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/category
