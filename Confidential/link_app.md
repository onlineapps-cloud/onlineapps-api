### POST /app/user/
* Description: Link app to user's account
* Auth: Bearer key
* Body: x-www-form-urlencoded: 
  ```
                              [uid -- user id
                               id  --  app id]
* Response:
    * 200: **SUCCESS**
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
    * 403: **ALREADY_LINKED**
    * 403: **INSUFFICIENT_FUNDS**
    * (404: NOT_FOUND)
* Example cURL:
  ```
    curl --request POST \
    --url https://requests.onlineapps.cloud/app/user/ \
    --header 'authorization: Bearer {{token}}' \
    --data uid=2
    --data id=35
