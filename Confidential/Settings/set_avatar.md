### POST /avatar/
- Description: Update user's avatar
- Auth: Bearer key
- Body: **IMPORTANT multipart/form-data**: `[avatar -- image file (jpg/png)]`
- Response:
    - 200: **SUCCESS**
    - 401: **INVALID_TOKEN**
    - 401: **IP_CHANGE**
    - 400: **NO_AVATAR**
- Example cURL:
  ```
curl --request POST \
  --url https://requests.onlineapps.cloud/avatar/2 \
  --header 'authorization: Bearer {{token}}' \
  --header 'content-type: multipart/form-data; boundary=---011000010111000001101001' \
  --form avatar=@/path/to/file
