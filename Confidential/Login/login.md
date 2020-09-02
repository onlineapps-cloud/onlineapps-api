### POST /login/ 
- Description: Check username, password/hash, OTP and return an auth token. If otp isn't provided check bindings
- Body: x-www-form-urlencoded: 
  ```
                               [username    -- username
                                hash        -- password hash
                                otp         -- OTP code
                                computer    -- name of PC
                                cpu         -- CPU ID Binding
                                mb          -- MotherBoard ID Binding
                                usb         -- USB ID Binding
                                win        -- Windows username binding]
                                (unbound variables MAY be excluded)

- Response:
    - 200: Bearer token (self-contained jwt, with login IP and **UID*-contained)
    - 401: **AUTHENTICATION_FAILED**
    - 401: **BINDING_FAILED**
- Example cURL:
  ```
    curl --request POST \
    --url https://requests.onlineapps.cloud/login/ \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data username=first \
    --data hash={{hash}} \
    --data otp={{otp}} \
  ```
OR WITH BINDINGS
  ```  
    curl --request POST \
    --url https://requests.onlineapps.cloud/login/ \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data username=first \
    --data hash={{hash}} \
    --data computer=mypc \
    --data mb="ATI-BFS234113LX1" \

