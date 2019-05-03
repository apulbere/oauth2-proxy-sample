## About
gateway / auth server / resource server

##### Example
obtain token
```
curl -X POST \
  http://localhost:8080/oauth/token \
  -H 'Authorization: Basic U3RyZXhDb3JwOnNtaWxpbmdfZ29k' \
  -d 'username=john&password=theFarmerPass&grant_type=password'
```
access resource
```
curl -X GET \
  http://localhost:8080/resource1/hello \
  -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE1NTY5MzA4NzMsInVzZXJfbmFtZSI6ImpvaG4iLCJhdXRob3JpdGllcyI6WyJST0xFX1VTRVIiXSwianRpIjoiYWMzNTcxOTQtNzM1OS00Njc4LTg0MTktZjdiNDZmNjBhODEwIiwiY2xpZW50X2lkIjoiU3RyZXhDb3JwIiwic2NvcGUiOlsiYWxsIl19.Hzjm8RSoDwTZTpA2Wz-mcJsS8KIHUC9f05obZvkCL7c'
```
