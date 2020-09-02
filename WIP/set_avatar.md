### POST /avatar/
- Description: Update user's avatar
- Auth: Bearer key
- Body: **IMPORTANT multipart/form-data**: 
  ```
                              [uid    -- user id
                               avatar -- image file (jpg/png)]
- Response:
    -200: **SUCCESS**
    -401: **INVALID_TOKEN**
    -401: **IP_CHANGE**
    -403: **NO_AVATAR**
- Example cURL:
  ```
curl --request POST \
  --url https://requests.onlineapps.cloud/avatar/ \
  --header 'authorization: Bearer {{token}}' \
  --header 'content-type: multipart/form-data; boundary=---011000010111000001101001' \
  --form uid=2 \
  --form avatar=@/path/to/file
