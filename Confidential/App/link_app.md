### POST /app/user/{{uid}}
- Description: Link app to user's account
- Auth: Bearer key
- Body: x-www-form-urlencoded: `[id -- app id]`
- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    - 403: **ALREADY_LINKED**
    - 403: **INSUFFICIENT_FUNDS**
    - 404: **NOT_FOUND**
- Example cURL:
  ```
    curl --request POST \
    --url https://requests.onlineapps.cloud/api/app/user/2 \
    --header 'authorization: Bearer {{token}}' \
    --data id=35
