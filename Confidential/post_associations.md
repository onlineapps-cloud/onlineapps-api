### POST /associations/
* Description: List Apps associated to certain extensions
* Auth: Bearer key
* Body: x-www-form-urlencoded: 
  ```
                               [uid          -- uid
								associations -- {"extension":"app name", "extension":"app name", ...}]
* Response:
    * 200: **SUCCESS**
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request POST \
  --url http://requests.onlineapps.cloud:1880/associations/ \
  --header 'authorization: Bearer eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6Ii9kYXRhL2ZpZXMva2V5cy9qd3RfcHJpdl9rZXkifQ.eyJzdWIiOiI2NTcyNDMiLCJpcCI6IjE4OC4xMzguMjM1LjIxNCIsImlzcyI6Ik9ubGluZSBBcHBzIiwiaWF0IjoxNTk2ODg1MTE3LCJleHAiOjE1OTY5MjgzMTd9.6qWLwmIHOV7wcbM-7zlA97gEi8SL1XAWXiX6x1kLWaLt1humAXQKiVxcidq4Ku5x-UOk2kddZ_iJxb3IkL7w4U8NXnX-D2fzaDhGX0ZjbbRpkQvmoVIw9PdGYPM_8I9Enkxpcwb9Cdxkd4XecQ02KlGCaBOMvlv2wTPKNLgoN6PUiGyfEvRjosG_XtGZgOCt0bwQ1Q5FEhC3veHjYOr4JjSJ_8Hqc0Pt28youLEuivDedKzroG1j1MEl-7veH3SSh_wg6hBmzPylxWr-sx1rDpw7vZkPFrPGrLx6kLkvKI9tkg8Pc4s1UXIlMv7nu6by7LUFrJsz8xercx32mTunWmLUmLknjIIyKTzm5U96e1DaZERMbfxx2_pXucy4Kh29TEecS-HBAjBMqh1Xp-6O6HUnT85VFwtY3vvsx_mQXLEYCWEBAtrFpddvo-wg1pA1cawqXiziU919rXxUDUFa3ib05-r28uIvKYHxGNQbVDShge28krylO3Tys_f0gH1H1trIiANIiQkSRvGgFHrmFZ4InZKyM4QCiIrw0eGIuMzFvaoSeOxO-NsdLMLU2dh35GE-SLXaCoI8DYBXbXqlkpDCG6GJNNUE5BDr1yaerwPPEARz5RQKytXvGjIRsGfRkWPuHgAGyWB3GO8BmsGDlkZHLBRRCCBxmX-eznn6vBg' \
  --header 'content-type: application/x-www-form-urlencoded' \
  --data uid=657243 \
  --data 'associations={"dwg":"ZWCAD"}'
