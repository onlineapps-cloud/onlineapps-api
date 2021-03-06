### PATCH /user/{{uid}}
- Description: Check otp if enabled; update account
- Auth: Bearer key
- Body: x-www-form-urlencoded: 
  ```
                               [otp         -- one time auth code
                                email       -- new email
                                phone       -- new phone
                                password    -- new password]
                                (excluded variables will not be updated)

- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    - 401: **OTP_FAILED**
    - 400: **MALFORMED_EMAIL**
    - 422: **EXISTING_EMAIL**
    - 400: **MALFORMED_PASSWORD**
    - 400: **MALFORMED_PHONE**
- Example cURL:
  ```
  curl --request PATCH \
  --url https://requests.onlineapps.cloud/api/user/2 \
  --header 'content-type: application/x-www-form-urlencoded' \
  --header 'authorization: Bearer {{token}}' \
  --data password=Newp4ss \
  --data 'phone=+9999' \
  --data email=aaa@ddd.vvvs \
  --data otp=368350 \

