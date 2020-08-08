### GET /app/rdp/user/{{uid}}
* Description: List all apps purchased by a user for rdp.json
* Auth: Bearer key
* Response:
    * 200: `[{name       : 'App name'}, ...]`
    * 401: **INVALID_TOKEN**
    * 401: **IP_CHANGE**
* Example cURL:
  ```
    curl --request GET \
    --url http://requests.onlineapps.cloud:1880/app/rdp/user/2 \
    --header 'authorization: Bearer eyJhbGciOiJSUzUxMiIsInR5cCI6IkpXVCIsImtpZCI6InJzYV9wcml2X2tleSJ9.eyJzdWIiOiJmaXJzdCIsImlzcyI6Ik9ubGluZSBBcHBzIiwiaWF0IjoxNTk2NDU3MzA2LCJleHAiOjE1OTY0NTc5MDZ9.mhqb3QLnCLBnac0xB281Wig_OidLk_dkeQWWyM7rOGcifjMBBr3grM1nuUQQvwtytgMNPFKLmsg9-anwYNyY_eNPxCOyiGedvOcIny46-EnFud8DDN6go1xivNYIlXQ1RcSANAKrzZKkU6MQhiJWPsPMst847UjKSRL8ZjFjZHjsVHV8sCrxGLDwq3MIjF7g2acqLPLmq34aGnrCPR-2dPraNdDBAQiRLgkMt1VMEI0v2TVmSDPo3tnKIByV-Q76g2EQJFEotnhCoizTNiM9sd0LOi4nbo3MaxqBYFWyTS2XZ3yVqxC4MeEeDX9wNpmUEwaJmXh4GCGkqw58hlHX9ei077s0eVfG81ntIUiMjn-rFClC5oeLqnc5rwbsCvyl0DYgSYiDn3oVgik9bQ1-x3Vd-NxCIRbEDugq7AZ9enCbzIKFCIXsGe2oriluaWh4Glulo-tKKU164VVUUIDmkH11TyO8NJbjIg90oZQ2Ff8UFUiKddIs5GxYhfh_M1REtuRl5R8lt5mzFP5tRQktVNcZ7mrblC446rtK9Ve0OXCrgLzCbmt8qgMQcogdSuVDjD8Ktdp9VEamTXbslJOB_F4Plth3Bs1EXzwYKgP2dQJWu1lBa2tsYWBVShr08IA9B3QqqmfkRBSeAe8_OgQMWdbyZa-RSQmTiGMWEqkzDHM'
