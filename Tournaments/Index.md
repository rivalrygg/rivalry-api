# Get tournament information

## Endpoint

`GET https://api.rivalry.com/api/v1/tournaments`

## Response format

On success, the HTTP status code in the response header is `200` and the response contains an array of [tournament objects](../Objects.md#tournament).

### Query parameters:

KEY | Value | Value description
--- | --- | ---
game_id | [game object](../Objects.md#game) id | Scope returned tournaments to a specific game

### Example:

```json
{
  "data": [
    {
      "id": 111,
      "name": "ESL Pro League",
      "game": {
        "id": 21,
        "name": "Counter-Strike"
      }
    }
  ],
  "links": {
    "first": "https://rivalry.com/api/v1/tournaments?page=1",
    "last": "https://rivalry.com/api/v1/tournaments?page=1",
    "prev": null,
    "next": null
  },
  "meta": {
    "current_page": 1,
    "from": 1,
    "last_page": 1,
    "path": "https://rivalry.com/api/v1/tournaments",
    "per_page": 15,
    "to": 15,
    "total": 1
  }
}
```
