### POST /associations/
* Description: List Apps associated to certain extensions
* Auth: Bearer key
* Body: x-www-form-urlencoded: 
  ```
                               [uid          -- uid
								associations -- {"extension":"app name", "extension":"app name", ...}]
* Response:
    * 200: **SUCCESS**
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request POST \
  --url https://requests.onlineapps.cloud/associations/ \
  --header 'authorization: Bearer {{token}}' \
  --data uid=657243 \
  --data 'associations={"dwg":"ZWCAD"}'
