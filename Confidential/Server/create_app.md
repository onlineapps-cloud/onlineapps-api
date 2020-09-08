### POST /server/app/{{uid}}
- Auth: Bearer key
- Description: Create a new custom app
- Body: **IMPORTANT multipart/form-data**: 
  ```
                               [name       -- app name
                                servers    -- ["ip", "ip", ...]
                                extensions -- ["ext","ext", ...]
                                categories -- [categoryID, categoryId, ...]
                                icon       -- ico/jpg/png file ]
- Response:
  - 200: **SUCCESS**
  - 422: **EXISTING_APP**
  - 400: **MALFORMED_JSON** ('var' identifies which variable is wrong)
  - 400: **MALFORMED_NAME**
  - 400: **MALFORMED_IP**
  - 400: **MALFORMED_EXTENSION**
  - 400: **MALFORMED_CATEGORY**
  - 404: **NOT_FOUND** ('var' identifies which variable is wrong)
  - 422: **LIMIT_EXCEEDED** ('var' identifies which variable is wrong)
