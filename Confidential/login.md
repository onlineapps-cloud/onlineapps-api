### POST /login/ 
* Description: Check uername and password/hash and return an auth token
* Body: x-www-form-urlencoded: 
  ```
                               [username    -- username
                                password    -- plaintext password or
                                hash        -- password hash (described later)
                                computer    -- name of PC]
* Response:
    * 200: Bearer token (self-contained jwt, with login IP and **UID** contained)
    * 401: **AUTHENTICATION_FAILED**
* Example cURL:
  ```
    curl --request POST \
    --url https://requests.onlineapps.cloud/login/ \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data username=first \
    --data password={{password}} \
    --data computer=mypc \
  ```
OR WITH HASH
  ```  
    curl --request POST \
    --url https://requests.onlineapps.cloud/login/ \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data username=first \
    --data hash={{hash}} \
    --data computer=mypc \

