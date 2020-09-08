### DELETE /server/{{uid}}
- Description: Delete a server
- Auth: Bearer key
- Body: x-www-form-urlencoded: `[ip -- server ip]`
- Response:
    - 200: **SUCCESS**
    - 404: **NOT_FOUND**
- Example cURL:
  ```
    curl --request DELETE \
    --url https://requests.onlineapps.cloud/api/server/2 \
    --header 'authorization: Bearer {{token}}' \
    --data ip=127.0.0.1