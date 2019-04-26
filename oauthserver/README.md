### About
OAuth 2 authorization server

#### Prerequisites
* Java 11

##### Examples

* access token for StrexCorp client

request
```
curl -X POST \
  http://localhost:8080/oauth/token \
  -H 'Authorization: Basic U3RyZXhDb3JwOnNtaWxpbmdfZ29k' \
  -d 'username=john&password=theFarmerPass&grant_type=password'
```
response
```
{
    "access_token": "3c369ded-7a34-4c64-ae93-7c0b0b875726",
    "token_type": "bearer",
    "refresh_token": "356f5fa0-8e16-4d4c-a5dd-44e0f2e28383",
    "expires_in": 43199,
    "scope": "all"
}
```
* refresh token for StrexCorp client


request

```
curl -X POST \
  http://localhost:8080/oauth/token \
  -H 'Authorization: Basic U3RyZXhDb3JwOnNtaWxpbmdfZ29k' \
  -d 'grant_type=refresh_token&client_id=StrexCorp&refresh_token=99540798-83b0-4b12-ab2c-e786dc4936c7'
```
response
```
{
    "access_token": "d17a0788-a34d-4d07-aa51-839f3b7416c7",
    "token_type": "bearer",
    "refresh_token": "99540798-83b0-4b12-ab2c-e786dc4936c7",
    "expires_in": 43199,
    "scope": "all"
}
```
* access token for DesertBluffs client (no Basic Auth)

request
```
curl -X POST \
  http://localhost:8080/oauth/token \
  -d 'username=john&password=theFarmerPass&grant_type=password&client_id=DesertBluffs'
```
response
```
{
    "access_token": "031fb984-278f-4c29-8ae9-232eb1547bfb",
    "token_type": "bearer",
    "refresh_token": "cd110330-f0c3-4761-af79-f7ee93fb47b4",
    "expires_in": 43127,
    "scope": "all"
}
```
* refresh token for DesertBluffs client

request
```
curl -X POST \
  http://localhost:8080/oauth/token \
  -d 'grant_type=refresh_token&client_id=DesertBluffs&refresh_token=cd110330-f0c3-4761-af79-f7ee93fb47b4'
```
response
```
{
    "access_token": "5702b3e3-7323-43d5-b60b-b36f785448c8",
    "token_type": "bearer",
    "refresh_token": "cd110330-f0c3-4761-af79-f7ee93fb47b4",
    "expires_in": 43199,
    "scope": "all"
}
```