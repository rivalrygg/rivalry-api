# Get tournament information

## Endpoint

`GET https://api.rivalry.com/api/v1/tournaments/{id}`

## Response format

On success, the HTTP status code in the response header is `200` and the response contains the `JSON` data for the specified match.

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
name | string | Tournament name
game | [game object](../Objects.md#game) | Game object
matches | array of [match objects](../Objects.md#match) | Full match objects

### Example:

```json
{
  "data": {
    "id": 191,
    "name": "LCS NA",
    "game": {
      "id": 24,
      "name": "League of Legends"
    },
    "matches": [
      {
        "id": 482,
        "url": "https://rivalry.com/match/league-of-legends/lcs-na/482-clutch-gaming-vs-echo-fox",
        "scheduled_at": "2018-06-17T21:25:00Z",
        "competitors": [
          {
            "id": 293,
            "name": "Clutch Gaming"
          },
          {
            "id": 292,
            "name": "Echo Fox"
          }
        ]
      }
    ]
  }
}
```
