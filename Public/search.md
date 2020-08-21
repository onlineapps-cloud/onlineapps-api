### GET /app/search/{{query}}
* Description: List all app names containing the query
* Response:
    * 200:  ` [name, ...] `
* Example cURL:
  ```
    curl --request GET \
    --url https://requests.onlineapps.cloud/app/search/word
