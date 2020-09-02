### POST /bind/{{uid}}
- Description: Update bindings
- Auth: Bearer key
- Body: x-www-form-urlencoded: 
  ```
                               [cpu    -- CPU ID Binding
                                mb     -- MotherBoard ID Binding
                                usb    -- USB ID Binding
                                win    -- Windows user Binding
                                bindIP -- 1 - bind IP, 0 - unbind IP
                                otp    -- one time auth code]
                                (excluded variables will be unbound.
                                 IP is decoded from request, to unbind it 
                                 set bindIP to 0)

- Response:
    - 200: **SUCCESS**
    - 401: **OTP_DISABLED**
    - 401: **OTP_FAILED**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
- Example cURL:
  ```
    curl --request POST \
    --url https://requests.onlineapps.cloud/bind/2 \
    --header 'authorization: Bearer {{token}}' \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data computer=mypc \
    --data mb="ATI-BFS234113LX1" \
    --data otp="553055"
  ```
