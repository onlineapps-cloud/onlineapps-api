### GET /app/rdp/user/{{uid}}
- Description: List all apps purchased by a user for rdp.json
- Auth: Bearer key
- Response:
    - 200: `[{name : 'App name'}, ...]`
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/app/rdp/user/2 \
    --header 'authorization: Bearer {{token}}'
