### PATCH /user/ 
* Description: Check username, password/hash, otp; update account
* Body: x-www-form-urlencoded: 
  ```
                               [username    -- username
                                password    -- plaintext password or
                                hash        -- password hash
                                otp         -- one time auth code
                                email       -- new email
                                phone       -- new phone
                                newpassword -- suprisingly, new password]
                                (excluded variables will be unbound.
                                 IP is decoded from request, to unbind it 
                                 set bindIP to 0)

* Response:
    * 200: **SUCCESS**
    * 401: **AUTHENTICATION_FAILED**
    * 401: **WRONG_OTP**
* Example cURL:
  ```
  curl --request PATCH \
  --url https://requests.onlineapps.cloud/user/ \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data username=goban \
  --data password=P4sswodr \
  --data newpassword=Newp4ss \
  --data 'phone=+9999' \
  --data email=aaa@ddd.vvvs \
  --data otp=368350 \

