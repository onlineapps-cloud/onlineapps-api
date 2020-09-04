### GET /user/{{username_or_email}}
- Description: Check if username or email exists
- Response:
    - 200: **EXISTING_USERNAME**
    - 200: **EXISTING_EMAIL**
    - 200: **AVAILABLE_USERNAME**
    - 200: **AVAILABLE_EMAIL**
    - 404: **NOT_VALID**
- Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/user/first
