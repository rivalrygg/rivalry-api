# Objects

A full list of the objects returned by the endpoints of the Rivalry.gg API.

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
