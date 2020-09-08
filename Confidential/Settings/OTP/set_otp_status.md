### POST /otp/status/{{uid}}
- Description: CHech OTP, Enable/disable it
- Auth: Bearer key
- Body: x-www-form-urlencoded: 
  ```
    [ 
      status -- 0/1
- Response:
    - 200: **SUCCESS**
    - 400: **INVALID_STATUS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    - 401: **OTP_FAILED**
    
- Example cURL:
  ```
    curl --request POST \
  --url https://requests.onlineapps.cloud/api/otp/status/2 \
  --header 'authorization: Bearer {{token}}' \
  --data 'status=0'
