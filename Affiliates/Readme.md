# Affiliate program

## Authentication

Accessing affiliate endpoints requires that you pass you affiliate API key as a `api_key` GET parameter:
`/v1/affiliates/stats?api_key={your key}`

API key can be obtained on affiliate tab of your profile.

## Available endpoints

Endpoints for retrieving affiliate information

Base URL: `https://www.rivalry.gg/api`

Method | Endpoint | Usage | Returns
--- | --- | --- | ---
GET | [`/v1/affiliates/stats`](Stats.md) | Get affiliate report | [affiliate report](../Objects.md#affiliate-report)