# Get match information

## Endpoint

`GET https://www.rivalry.com/api/v1/matches`

## Response format

On success, the HTTP status code in the response header is `200` and the response contains an array of [match objects](../Objects.md#match).

### Query parameters:

KEY | Value | Value description
--- | --- | ---
game_id | [game object](../Objects.md#game) id | Scope returned matches to a specific game
tournament_id | [tournament object](../Objects.md#tournament) id | Scope returned matches to a tournament

### Example:

```json
{
  "data": [
    {
      "id": 399,
      "url": "https://rivalry.com/match/league-of-legends/lcs-eu/399-unicorns-of-love-vs-misfits",
      "scheduled_at": "2018-06-16T16:00:00Z",
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
          "id": 273,
          "name": "Unicorns of Love"
        },
        {
          "id": 270,
          "name": "Misfits"
        }
      ],
      "markets": [
        {
          "id": 441,
          "name": "winner",
          "outcomes": [
            {
              "id": 779,
              "odds": 2.23,
              "competitor": {
                "id": 273,
                "name": "Unicorns of Love"
              }
            },
            {
              "id": 780,
              "odds": 1.54,
              "competitor": {
                "id": 270,
                "name": "Misfits"
              }
            }
          ]
        }
      ]
    }
  ],
  "links": {
    "first": "https://rivalry.com/api/v1/matches?page=1",
    "last": "https://rivalry.com/api/v1/matches?page=3",
    "prev": null,
    "next": "https://rivalry.com/api/v1/matches?page=2"
  },
  "meta": {
    "current_page": 1,
    "from": 1,
    "last_page": 3,
    "path": "https://rivalry.com/api/v1/matches",
    "per_page": 15,
    "to": 15,
    "total": 37
  }
}
```
