### PATCH /otp/{{uid}}
- Description: Unlink an app
- Auth: Bearer key
- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request PATCH \
    --url http://requests.onlineapps.cloud/otp/2 \
    --header 'authorization: Bearer {{token}}' \

