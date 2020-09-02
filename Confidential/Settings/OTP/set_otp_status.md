### POST /otp/status/{{uid}}
- Description: List Apps associated to certain extensions
- Auth: Bearer key
- Body: x-www-form-urlencoded: `status -- 0/1`
- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    
- Example cURL:
  ```
    curl --request POST \
  --url https://requests.onlineapps.cloud/otp/status/2 \
  --header 'authorization: Bearer {{token}}' \
  --data 'status=0'
