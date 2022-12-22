# Get game information

## Endpoint

`GET https://api.rivalry.com/api/v1/matches/{id}`

## Response format

On success, the HTTP status code in the response header is `200` and the response contains the `JSON` data for the specified match.

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
url | string | Rivalry match URL
scheduled_at | Timestamp | Match start time
tournament | [tournament object](../Objects.md#tournament) | Tournament object
competitors | array of [competitor objects](../Objects.md#competitor) | Competitor objects
markets | array of [market objects](../Objects.md#market) | Market objects
game | [game object](../Objects.md#game) | Game object


### Example:

```json
{
  "data": {
    "id": 366,
    "url": "https://rivalry.com/match/league-of-legends/lpl/366-funplus-phoenix-vs-snake-esports",
    "scheduled_at": "2018-06-15T11:00:00Z",
  	"game": {
  		"id": 24,
  		"name": "League of Legends"
  	},
    "tournament": {
      "id": 212,
      "name": "GSL Season 2 Code S, Playoffs"
    },
    "competitors": [
      {
        "id": 267,
        "name": "Funplus Phoenix"
      },
      {
        "id": 245,
        "name": "Snake Esports"
      }
    ],
    "markets": [
      {
        "id": 322,
        "name": "winner",
        "outcomes": [
          {
            "id": 539,
            "odds": 1.96,
            "competitor": {
              "id": 267,
              "name": "Funplus Phoenix"
            }
          },
          {
            "id": 540,
            "odds": 1.7,
            "competitor": {
              "id": 245,
              "name": "Snake Esports"
            }
          }
        ]
      }
    ]
  }
}
```
