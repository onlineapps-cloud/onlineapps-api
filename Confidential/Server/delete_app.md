### DELETE /server/app/{{uid}}
- Description: Delete an app
- Auth: Bearer key
- Body: x-www-form-urlencoded: `[id -- app id]`
- Response:
    - 200: **SUCCESS**
    - 404: **NOT_FOUND**
- Example cURL:
  ```
    curl --request DELETE \
    --url https://requests.onlineapps.cloud/api/server/app/2 \
    --header 'authorization: Bearer {{token}}' \
    --data id=1