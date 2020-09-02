### PATCH /user/ 
- Description: Check username, password/hash, otp; delete account
- Body: x-www-form-urlencoded: 
  ```
                               [username    -- username
                                password    -- plaintext password or
                                hash        -- password hash
                                otp         -- one time auth code]

- Response:
    -200: **SUCCESS**
    -401: **AUTHENTICATION_FAILED**
    -401: **WRONG_OTP**
- Example cURL:
  ```
curl --request DELETE \
  --url https://requests.onlineapps.cloud/user/ \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data username=goban \
  --data password=P4ssword
