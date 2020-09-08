### GET /otp/status/{{uid}} 
- Description: Return OTP status
- Auth: Bearer key
- Response:
    - 200: {enabled: 0/1}
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/otp/status/3 \
    --header 'authorization: Bearer {{token}}'
