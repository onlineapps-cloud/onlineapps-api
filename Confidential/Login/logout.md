### GET /logout/{{uid}}
- Description: Make token invalid
- Auth: Bearer key
- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url http://requests.onlineapps.cloud/api/login/2 \
    --header 'authorization: Bearer {{token}}' \
