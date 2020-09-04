### PATCH /user/{{uid}}
- Description: Check otp if enabled; delete account
- Auth: Bearer key
- Body: x-www-form-urlencoded:`[otp -- one time auth code]`

- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    - 401: **OTP_FAILED**
- Example cURL:
  ```
curl --request DELETE \
  --url https://requests.onlineapps.cloud/user/2 \
  --header 'content-type: application/x-www-form-urlencoded' \
  --header 'authorization: Bearer {{token}}' \
  --data otp=368350
