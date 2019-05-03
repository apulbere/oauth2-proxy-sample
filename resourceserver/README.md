### About
OAuth 2 resource server

#### Prerequisites
* Java 11

##### Example
request with Authorization header from `oauthserver` application
```
curl -X GET \
  http://localhost:8081/hello \
  -H 'Authorization: Bearer 0d4b819a-4d10-477f-96ec-6f4cbafecd93' \
```