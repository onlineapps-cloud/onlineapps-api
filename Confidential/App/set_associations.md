### POST /associations/{{uid}}
- Description: List Apps associated to certain extensions
- Auth: Bearer key
- Body: x-www-form-urlencoded: `[associations -- {"extension":"app id", "extension":"app id", ...}]`
- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    
- Example cURL:
  ```
    curl --request POST \
  --url https://requests.onlineapps.cloud/associations/2 \
  --header 'authorization: Bearer {{token}}' \
  --data 'associations={"dwg":"17"}'
