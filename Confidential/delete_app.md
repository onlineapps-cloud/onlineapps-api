### DELETE /app/user/
* Description: Unlink an app
* Auth: Bearer key
* Body: x-www-form-urlencoded: 
  ```
                              [uid -- user id
                               id  --  app id]
* Response:
    * 200: **SUCCESS**
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request DELETE \
    --url http://requests.onlineapps.cloud:1880/app/user/ \
    --header 'authorization: Bearer {{token}}' \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data uid=3
    --data id=34
