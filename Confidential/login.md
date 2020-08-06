### POST /login/<username>  
* Description: Check uername and password/hash and return an auth token
* Body: x-www-form-urlencoded: 
  ```
                               [password    -- plaintext password or
                                hash        -- password hash (described later)
                                computer    -- name of PC
                                country     -- full country name 
                                countryCode -- 2 letter code (MD)
                                city        -- city]
* Response:
    * 200: Token
    * 401: **AUTHENTICATION_FAILED**
* Example cURL:
  ```
    curl --request POST \
    --url http://requests.onlineapps.cloud:1880/login/first \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data password=WrongPass \
    --data computer=mypc \
    --data country=Moldova \
    --data countryCode=MD \
    --data city=Chisinau
  ```
OR WITH HASH
  ```  
    curl --request POST \
    --url http://requests.onlineapps.cloud:1880/login/first \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data hash=55e5905c94271a1064b3ffc065387c917af21b8db9f41a63c4a78a49abc758f0e63369d8ab91b40419ba2c105d65f309313ac30812961dedca2a7a24f2505582 \
    --data computer=mypc \
    --data country=Moldova \
    --data countryCode=MD \
    --data city=Chisinau
