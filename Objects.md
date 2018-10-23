# Objects

A full list of the objects returned by the endpoints of the [Rivalry.gg](https://www.rivalry.gg/) API.

A key starting with `?` represents data that is not included in all endpoints. For reference what the endpoints include see [available endpoints](../).

## Game

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
name | string | Game name
?matches | array of [match objects](#match) | Game matches

## Match

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
url | string | Rivalry.gg match URL
scheduled_at | Timestamp | Match start time
?tournament | [tournament object](#tournament) \| null | Match related tournament
?competitors | array of [competitor objects](#competitor) | Competitors playing in the match
?markets | array of [market objects](#market) | Open markets for the match

## Competitor

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
name | string | Competitor name

## Market

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
name | string \| null | Market name
?outcomes | array of [outcome objects](#outcome) | Market outcomes

## Outcome

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
odds | float | Outcome odds
?competitor | [competitor object](#competitor) \| null | Outcome related competitor

## Tournament

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
name | string | Tournament name
?game | [game object](#game) \| null | Tournament game
?matches | array of [match objects](#match) | Tournament matches

## Affiliate report

KEY | Value type | Value description
--- | --- | ---
start_date | string | Report period start
end_date | string | Report period end
num_users_joined | int | Number of users joined in the selected period
num_users_deposited | string | Number of users deposited in the selected period
amount_deposited | int (USD cents) | Amount deposited in the selected period
amount_wagered | int (USD cents) | Amount wagered in the selected period
ggr_revenue | int (USD cents) | Gross gambling revenue
net_revenue | int (USD cents) | Net affiliate revenue
?subcode_id | int | Subcode identifier (only when showing statistics for a specific subcode)

## Affiliate subcode

KEY | Value type | Value description
--- | --- | ---
id | int | Identifier
code | string | Code