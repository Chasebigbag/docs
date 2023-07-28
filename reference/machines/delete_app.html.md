```
curl -i -X DELETE \\
    -H "Authorization: Bearer ${FLY\_API\_TOKEN}" -H "Content-Type: application/json" \\
    "${FLY\_API\_HOSTNAME}/v1/apps/my-app-name" 

```
**Status: 404**
```json
{
  "error": "Could not find App \"my-app-name\""
}
```