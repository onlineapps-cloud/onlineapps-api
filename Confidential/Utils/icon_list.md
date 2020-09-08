### GET /icons/{{uid}}
- Description: Return array of all user's app icons 
- Auth: Bearer key
- Response:
    - 200: ["url", "url", ...]
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/icons/3 \
    --header 'authorization: Bearer {{token}}'
