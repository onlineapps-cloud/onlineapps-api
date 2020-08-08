### POST /user/
* Description: Create a new individual user
* Body: x-www-form-urlencoded: 
  ```
                               [username -- username
                                password -- plaintext password 
                                phone    -- optional, can have +,(),- 
                                email    -- unique email]
* Response:
    * 200: **SUCCESS**
    * 422: **EMAIL_REQUIRED**
    * 422: **MALFORMED_USERNAME**
    * 422: **EXISTING_USERNAME**
    * 422: **MALFORMED_EMAIL**
    * 422: **EXISTING_EMAIL**
    * 422: **MALFORMED_PASSWORD**
    * 422: **MALFORMED_PHONE**
* Example cURL:
  ```
    curl --request POST \
    --url http://requests.onlineapps.cloud:1880/user/ \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data username=Third \    
    --data password=TestPass123 \
    --data email=asss@asss.as \
    --data 'phone=+1111'
