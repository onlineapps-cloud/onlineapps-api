### POST /app/user/<username> 
* Description: Link app to user's account
* Auth: Bearer key
* Body: x-www-form-urlencoded: `[id -- app id]`
* Response:
    * 200: **SUCCESS**
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
    * 403: **ALREADY_LINKED**
    * 403: **INSUFFICIENT_FUNDS**
* Example cURL:
  ```
    curl --request POST \
    --url http://requests.onlineapps.cloud:1880/app/user/first \
    --header 'authorization: Bearer eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6InJzYV9wcml2X2tleSJ9.eyJzdWIiOiJmaXJzdCIsImlzcyI6Ik9ubGluZSBBcHBzIiwiaWF0IjoxNTk2NDU3NDYzLCJleHAiOjE1OTY0NTgwNjN9.YiebqO-I0BvDZleYT0uU9eDjr2i2VY-uYHghGWBSwnWq7iz9ssEaZLwJoV4vGSe_nvEdx_xVPNdtVtb1W_IJFFUUnofn4a_8CknK9VJqXvzwSp4-B32N5YfgX3s2Ku9H4TTMwVydSb3N73pkyCwx9R4Ic6RcqxHuGtMLUfUNVBbjII7cuNX9AV4LDyi-qlkQKqvArrpdVzYphkX2h-21M3fHAPe_xqSUo_pl8V7YBjBD03OpToYdHD74fk2QOJ7YRdDBVlc8hKguHiT3ekQciE1tK5m8WAVt9VGYSMPbeVbpIVfMDJXEBn2pWkJK4KP27u8nOVgKZbu3lN15cRlNbQOcvrAx1j988id4ZCoaJaHtjod3RGDOA6-1Fo2Suoq6Bk1ztggUUSkj4MTt3asV8xY87DRpkaZNAE3uscUm9GsQ40gIDbiacJMCCNUlxHO1RPIMrqUPOdoqgOG97gEi5Eb7xGtQKwX_X6L6rS6jHuf5yHG329ZkJQHTLBcOv-wKCf0o4K6ZUXlQExgNRJIrQkjEQ2rK3qUmNUwp56I9WwDbF35H20RbT5ESOng7zM0UQWCfMukMzvoLjR0dGQyzBhpf9HCH5HfTxNKRSiKzZLPyezo6XGk4kTLY-IFz4lw8Q9dBNryoFKpOQCR3s0DAgBCUDHKJT4wr5YaxGBWKH8s' \
    --header 'content-type: application/x-www-form-urlencoded' \
    --data id=35
