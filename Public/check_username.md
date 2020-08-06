### GET /user/<username_or_email>
* Description: Check if username or email exists
* Response:
    * 200: **EXISTS**
    * 404: **NOT_FOUND**
* Example cURL:
  ```
    curl --request GET \
    --url http://requests.onlineapps.cloud:1880/user/first
