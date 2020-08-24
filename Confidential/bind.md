### POST /bind/ 
* Description: Check username, password/hash, otp; update bindings and return an auth token
* Body: x-www-form-urlencoded: 
  ```
                               [username    -- username
                                password    -- plaintext password or
                                hash        -- password hash (described later)
                                computer    -- name of PC
                                cpu         -- CPU ID Binding
                                mb          -- MotherBoard ID Binding
                                usb         -- USB ID Binding
                                bios        -- BIOS version Binding
                                bindIP      -- 1 - bind IP, 0 - unbind IP
                                otp         -- one time auth code]
                                (excluded variables will be unbound.
                                 IP is decoded from request, to unbind it 
                                 set bindIP to 0)

* Response:
    * 200: Bearer token (self-contained jwt, with login IP and **UID** contained)
    * 401: **AUTHENTICATION_FAILED**
    * 401: **WRONG_OTP**
* Example cURL:
  ```
    curl --request POST \
    --url https://requests.onlineapps.cloud/bind/ \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data username=first \
    --data password={{password}} \
    --data computer=mypc \
    --data mb="ATI-BFS234113LX1" \
  ```
OR WITH HASH
  ```  
    curl --request POST \
    --url https://requests.onlineapps.cloud/bind/ \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data username=first \
    --data hash={{hash}} \
    --data computer=mypc \
    --data mb="ATI-BFS234113LX1" \

