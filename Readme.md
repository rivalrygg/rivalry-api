# Rivalry.gg API

## Available endpoints

Method | Endpoint | Usage | Returns
--- | --- | --- | ---
GET | [`/v1/games`](Games/Index.md) | Get several games | games
GET | [`/v1/games/{id}`](Games/Show.md) | Get a game | game

## Requests

The Rivalry.gg API is based on REST principles. Data resources are retrieved via standard HTTPS GET requests in UTF-8 format to an API endpoint.

## Responses

Rivalry.gg API returns all successful response data as a JSON object with HTTP status code `200`.

The requested data is always wrapped in a `data` field:

```json
{
	"data": {

	}
}
```

## Timestamps

Timestamps are returned in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format as [Coordinated Universal Time (UTC)](https://en.wikipedia.org/wiki/UTC_offset) with a zero offset: `YYYY-MM-DDTHH:MM:SSZ`.

## Pagination

Some endpoints return a paginated result set, taking page as a parameter: `https://www.rivalry.gg/api/v1/games?page=1`

When the results are paginated, pagination data will be added to the resource:

```json
{
	"links": {
		"first": "https://www.rivalry.gg/api/v1/games?page=1",
		"last": "https://www.rivalry.gg/api/v1/games?page=1",
		"prev": null,
		"next": null
	},
	"meta": {
		"current_page": 1,
		"from": 1,
		"last_page": 1,
		"path": "https://www.rivalry.gg/api/v1/games",
		"per_page": 15,
		"to": 7,
		"total": 7
	}
}
```

