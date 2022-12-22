# Get affiliate report

## Endpoint

`GET https://api.rivalry.com/api/v1/affiliates/stats`

## Query parameters:

Both date parameters are required. Subcode

KEY | Value | Value description
--- | --- | ---
start_date | date (YYYY-MM-DD) | Report period start
end_date | date (YYYY-MM-DD) | Report period end
code | string | Code

**Warning**
When no `code` is provided, the report will return cumulative results for all users registered with any or no subcodes. However, when `code` is provided, the returned report will include only results for users registered with that subcode.

## Response format

On success, the HTTP status code in the response header is `200` and the response contains the `JSON` data containing affiliate report for a selected time period.

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
start_date | string | Report period start
end_date | string | Report period end
num_users_joined | int | Number of users joined in the selected period
num_users_deposited | string | Number of users deposited in the selected period
amount_deposited | int (USD cents) | Amount deposited in the selected period
amount_wagered | int (USD cents) | Amount wagered in the selected period
ggr_revenue | int (USD cents) | Gross gambling revenue
net_revenue | int (USD cents) | Net affiliate revenue
?code | string | Code (only when showing statistics for a specific subcode)

### Example:

```json
{
	"data": {
		"start_date": "2018-01-01",
		"end_date": "2018-09-15",
		"num_users_joined": 4903,
		"num_users_deposited": 5906,
		"amount_deposited": 516000,
		"amount_wagered": 0,
		"ggr_revenue": 495700,
		"net_revenue": 99140,
		"code": null
	}
}
```
