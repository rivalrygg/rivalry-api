# Get game information

## Endpoint

`GET https://www.rivalry.gg/api/v1/games`

## Response format

On success, the HTTP status code in the response header is `200` and the response contains an array of [game objects](../Objects.md#game).

### Example:

```json
{
	"data": [
		{
			"id": 20,
			"name": "Call of Duty"
		},
		{
			"id": 21,
			"name": "Counter-Strike"
		},
		{
			"id": 22,
			"name": "Dota 2"
		},
		{
			"id": 23,
			"name": "Hearthstone"
		},
		{
			"id": 24,
			"name": "League of Legends"
		},
		{
			"id": 25,
			"name": "Overwatch"
		},
		{
			"id": 26,
			"name": "StarCraft"
		}
	],
	"links": {
		"first": "https://rivalry.dev/api/v1/games?page=1",
		"last": "https://rivalry.dev/api/v1/games?page=1",
		"prev": null,
		"next": null
	},
	"meta": {
		"current_page": 1,
		"from": 1,
		"last_page": 1,
		"path": "https://rivalry.dev/api/v1/games",
		"per_page": 15,
		"to": 7,
		"total": 7
	}
}
```