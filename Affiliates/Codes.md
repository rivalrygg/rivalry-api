# Get affiliate's subcodes

## Endpoint

`GET https://www.rivalry.com/api/v1/affiliates/codes`

## Response format

On success, the HTTP status code in the response header is `200` and the response contains the `JSON` data containing affiliate report for a selected time period.

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
code | string | Code

### Example:

```json
{
	"data": {
		"code": "GreenPanda"
	}
}
```
