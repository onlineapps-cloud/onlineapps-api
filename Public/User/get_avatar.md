### GET /avatar/{{uid}}/{{s|m|l}}
- Description: Get user's avatar of a specified size (**s**mall, **m**edium, **l**arge)
- Response:
    - 200: 32x32/64x64/128x128 jpg image
    - 403: **WRONG_SIZE**
    - 404: **NOT_FOUND**
- Example cURL:
  ```
  curl --request GET \
  --url https://requests.onlineapps.cloud/avatar/2/m
