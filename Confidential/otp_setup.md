### GET /otp/{{uid}} 
* Description: Return link for otp auth setup
* Auth: Bearer key
* Response:
    * 200: link for otp auth setup
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/otp/3 \
    --header 'authorization: Bearer {{token}}'
