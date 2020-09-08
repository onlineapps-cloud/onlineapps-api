### POST /server/{{uid}}
- Description: Create a server
- Auth: Bearer key
- Body: x-www-form-urlencoded: `[ip -- server ip]`
- Response:
    - 200: **SUCCESS**
    - 400: **MALFORMED_IP**
    - 422: **EXISTING_IP**
- Example cURL:
  ```
    curl --request POST \
    --url https://requests.onlineapps.cloud/api/server/2 \
    --header 'authorization: Bearer {{token}}' \
    --data ip=127.0.0.1
