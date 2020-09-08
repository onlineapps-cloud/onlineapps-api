### DELETE /app/user/{{uid}}
- Description: Unlink an app
- Auth: Bearer key
- Body: x-www-form-urlencoded: [id -- app id]
- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    - 400: **INVALID_ID**
- Example cURL:
  ```
    curl --request DELETE \
    --url http://requests.onlineapps.cloud/app/user/2 \
    --header 'authorization: Bearer {{token}}' \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data id=34
