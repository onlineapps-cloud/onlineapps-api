### DELETE /avatar/
* Description: Delete user's avatar
* Auth: Bearer key
* Body: x-www-form-urlencoded: 
  ```
                              [uid    -- user id
                               avatar -- image file (jpg/png)]
* Response:
    * 200: **SUCCESS**
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
curl --request DELETE \
  --url https://requests.onlineapps.cloud/avatar/ \
  --header 'authorization: Bearer {{token}}' \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data uid=2
