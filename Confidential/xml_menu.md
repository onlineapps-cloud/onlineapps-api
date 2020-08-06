### GET /xml/menu/<username> 
* Description: Return menu.xml
* Auth: Bearer key
* Response:
    * 200: menu.xml
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL: 
  ```
    curl --request GET \
    --url http://requests.onlineapps.cloud:1880/xml/menu/first \
    --header 'authorization: Bearer eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6Ii9kYXRhL2ZpZXMva2V5cy9qd3RfcHJpdl9rZXkifQ.eyJzdWIiOiJmaXJzdCIsImlwIjoiMTg4LjEzOC4yMzUuMjE0IiwiaXNzIjoiT25saW5lIEFwcHMiLCJpYXQiOjE1OTY2MzA2NzMsImV4cCI6MTU5NjYzMTI3M30.hMQ0ejOdHFtG5-FkBgPVglntHJ3nLmiJ-KYVp9nTlUmxayujC1Qp7V_ICK5pkFIQeeR5CcnQWU-5SYF1VGhJySWkb1myWiUYfR56bR7-Y7z431X1ncvyRBmOTvT8RpEgn-pFGqchJiKJs0dFP3qltMCKSb5KaI1B_7F_vGCGMibV04Vb2DtwumpSSFgDCCNR2lzeEi2gS0PHC_IYbNSg4IXsibgJtSsTDdqWylqsAr2iSGtlmTGjJbC6yBqlDi5R8u3wtrS-Z2iaXvQw8kwdJNQ2vEyhyyzhK3DBvOW1negwX16Uka94r2vUOgATOMmAK0x1hZoi37lpGNxofAfxL5EB6D4tOUPnU29e-5cXKAUawDVGOqhfXe2aizBTIGpBMlIS5zRBypIipx_zC9QksjTT39A6uG4vk8o571Gzv0Fv7g6psqktP1u5oDOwo8eWNxQ-tc2U7gTrSIgiEMINig4bO3lMbsPA_SmDPNqQ3_m_8ZKv6crLUIzREd8fuTEjLs1BntGk3bGWHcgtcyuAgGz4Hz-_qXHc8Kw_gL_9Yu4_RXbmxcIsSMAoSZm4wIcvQX0oSrx9ynaUWVLWIuBHApekkX9okh-6ATRIUzgyYM8HASIYQuEii9mBwCDwFcJsXY_BjVNX61X5DSL2CT61ZIrQJgEJxoMgJJ0-vqXaabw'
  
