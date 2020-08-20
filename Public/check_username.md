### GET /user/<username_or_email>
* Description: Check if username or email exists
* Response:
    * 200: **EXISTS**
    * 404: **NOT_FOUND**
* Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/user/first
