#### How to use the provided `nonce`
Add the `fly-machine-lease-nonce` header to all subsequent API calls.
```
curl -i -X POST \
    -H "Authorization: Bearer ${FLY\_API\_TOKEN}" -H "Content-Type: application/json" -H "fly-machine-lease-nonce: fed368b018e9" \
    "${FLY\_API\_HOSTNAME}/v1/apps/my-app-name/machines/3d8d413b29d089/stop"
```
#### Release the lease
```
curl -i -X DELETE \
    -H "Authorization: Bearer ${FLY\_API\_TOKEN}" -H "Content-Type: application/json" -H "fly-machine-lease-nonce: fed368b018e9" \
    "${FLY\_API\_HOSTNAME}/v1/apps/my-app-name/machines/3d8d413b29d089/lease" 
```