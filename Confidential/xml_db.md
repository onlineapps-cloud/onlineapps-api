### GET /xml/db/{{uid}}
* Description: Return localapps.db.xml
* Auth: Bearer key
* Response:
    * 200: localapps.db.xml
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request GET \
    --url http://requests.onlineapps.cloud:1880/xml/db/2 \
    --header 'authorization: Bearer eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6Ii9kYXRhL2ZpZXMva2V5cy9qd3RfcHJpdl9rZXkifQ.eyJzdWIiOiJmaXJzdCIsImlwIjoiMTg4LjEzOC4yMzUuMjE0IiwiaXNzIjoiT25saW5lIEFwcHMiLCJpYXQiOjE1OTY2MzYwOTQsImV4cCI6MTU5NjYzNjY5NH0.jxYLOp5xcW3sIz7EzebwbLwmVOT3V2fOwNtRCAdn33pJ8PqIXXRqWkcHVdaTnV_uwbK6a-Nj6XsJp01YeQfJOpg9mrYqB3arUDRMPH_I7g5z5PDnYLqVd8G-_rqcjk2DNj0TnUbmjYCZ0OmPOZd6d6nTPpJg2fqa3NG6UkgQq724Wn3sdN1WOYQ0I1-0Eoelchfd7No3rLntyJ8s918_LbB0z8p7WszsZ_rwRfNWa_1aabSJxa6kARJGFfxjdGZREO8crf4GadkpSnt64Ny3p_61ZxBlxSrabgxyX2OhEmhDHO3eEXfJOry3NKDgN9uojLbJQn22fmAvKiU-MAnDhsDjYwOojlCnhhth8bG9IyopZxYj1oT7-7lYaPCyr6OuqzyDvjeNnyuCZCxLwHZNr-FG0gBTGdlN46LPE6CbfqoCPkAYkcY9JV1vk0clda57zfrg2NI8SUl6fTfE_zCOUd8OD4lilFHU0EPq8PcVXJd52LVlznCygSRPEq3hYKbLmdaXAf3xR0s-_vsvUwAAWRlUDHewWdd-v-8p07mplpqLTNY_RGnTmpzk_Tvrz0A8sD7LqNJfNG7RXaUWeFjO7Dc0NIv_MRb5LdTfllKEg779-Oi1E75KurCPWmdtclxCAfovhL-hdR_1mx1_UYdHAbgm7sybm7YnCYgIBK2m1EY'
