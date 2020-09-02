### GET /otp/status/{{uid}} 
- Description: Return link for otp auth setup
- Auth: Bearer key
- Response:
    - 200: {enabled: 0/1}
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/otp/status/3 \
    --header 'authorization: Bearer {{token}}'
