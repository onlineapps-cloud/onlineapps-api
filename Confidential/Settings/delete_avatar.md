### DELETE /avatar/{{uid}}
- Description: Delete user's avatar
- Auth: Bearer key

- Response:
    -200: **SUCCESS**
    -401: **INVALID_TOKEN**
    -401: **IP_CHANGE**
- Example cURL:
  ```
curl --request DELETE \
  --url https://requests.onlineapps.cloud/avatar/2 \
  --header 'authorization: Bearer {{token}}' \

