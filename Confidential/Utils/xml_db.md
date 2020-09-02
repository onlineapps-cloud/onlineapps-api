### GET /xml/db/{{uid}}
- Description: Return localapps.db.xml
- Auth: Bearer key
- Response:
    - 200: localapps.db.xml
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/xml/db/2 \
    --header 'authorization: Bearer {{token}}'
