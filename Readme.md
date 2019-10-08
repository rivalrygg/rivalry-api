# [Rivalry.com](https://www.rivalry.com/) API

## Available endpoints

Method | Endpoint | Usage | Returns
--- | --- | --- | ---
GET | [`/v1/games`](Games/Index.md) | Get several games | games
GET | [`/v1/games/{id}`](Games/Show.md) | Get a game | game
GET | [`/v1/matches`](Matches/Index.md) | Get several matches | matches
GET | [`/v1/matches/{id}`](Matches/Show.md) | Get a match | match
GET | [`/v1/tournaments`](Tournaments/Index.md) | Get several tournaments | tournaments
GET | [`/v1/tournaments/{id}`](Tournaments/Show.md) | Get a tournament | tournament
GET | [`/v1/affiliates/stats`](Affiliates/Stats.md) | Get affiliate's report | affiliate report
GET | [`/v1/affiliates/codes`](Affiliates/Codes.md) | Get affiliate's subcodes | affiliate subcodes

## Requests

The [Rivalry.com](https://www.rivalry.com/) API is based on REST principles. Data resources are retrieved via standard HTTPS GET requests in UTF-8 format to an API endpoint.

**The API rate limit is currently 60 requests/minute.**

## Responses

[Rivalry.com](https://www.rivalry.com/) API returns all successful response data as a JSON object with HTTP status code `200`.

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

Some endpoints return a paginated result set, taking page as a parameter: `https://www.rivalry.com/api/v1/games?page=1`

When the results are paginated, pagination data will be added to the resource:

```json
{
	"links": {
		"first": "https://www.rivalry.com/api/v1/games?page=1",
		"last": "https://www.rivalry.com/api/v1/games?page=1",
		"prev": null,
		"next": null
	},
	"meta": {
		"current_page": 1,
		"from": 1,
		"last_page": 1,
		"path": "https://www.rivalry.com/api/v1/games",
		"per_page": 15,
		"to": 7,
		"total": 7
	}
}
```

