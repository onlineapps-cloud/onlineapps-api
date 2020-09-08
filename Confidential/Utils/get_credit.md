### GET /credit/{{uid}}
- Description: Return users account balance
- Auth: Bearer key
- Response:
    - 200: Balance in USD
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/api/credit/3 \
    --header 'authorization: Bearer {{token}}'
