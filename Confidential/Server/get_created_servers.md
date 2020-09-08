### GET /server/{{uid}} 
- Description: List all servers created by a user
- Auth: Bearer key
- Response:
    - 200: `["ip", "ip", ...]`
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/server/2 \
    --header 'authorization: Bearer {{token}}'