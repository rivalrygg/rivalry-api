# Get game information

## Endpoint

`GET https://api.rivalry.com/api/v1/games/{id}`

## Response format

On success, the HTTP status code in the response header is `200` and the response contains the `JSON` data for the specified game.

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
name | string | Game name
matches | array of [match objects](../Objects.md#match) | Full match objects

### Example:

```json
{
	"data": {
		"id": 21,
		"name": "Counter-Strike",
		"matches":  [
			{
				"id": 294,
				"url": "https://rivalry.com/match/counter-strike/ecs-league/243-nrg-esports-vs-g-2-esports",
				"scheduled_at": "2018-06-09T18:00:00Z",
				"competitors": [
					{
						"id": 145,
						"name": "Crvena Zvezda",
						"abbreviation": "INF",
						"country": "RS"
					},
					{
						"id": 143,
						"name": "Toxic",
						"abbreviation": "TOX",
						"country": null
					}
				],
				"markets": [
					{
						"id": 270,
						"name": "winner",
						"outcomes": [
							{
								"id": 451,
								"odds": 1.74,
								"competitor": {
									"id": 145,
									"name": "Crvena Zvezda",
									"abbreviation": "INF",
									"country": "RS"
								}
							},
							{
								"id": 452,
								"odds": 1.91,
								"competitor": {
									"id": 143,
									"name": "Toxic",
									"abbreviation": "TOX",
									"country": null
								}
							}
						]
					}
				]
			},
		],
	}
}
```
