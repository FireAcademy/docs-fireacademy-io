# Using API Keys

catchpole has 3 different ways of getting an API key from a request. They are listed below based on priority - if the first one fails, the second one is tried, then the third one.

```go
func getAPIKeyForRequest(c *fiber.Ctx) string {
    api_key := c.Params("api_key")
    if api_key == "" {
        api_key = c.Get("X-API-Key")
    }
    if api_key == "" {
        api_key = c.Query("api-key")
    }

    return api_key
}
```



Note: We'll be using `1a7d0060-2d5a-473d-a8aa-a2cb0c277a31` as an example API key. Replace this with the API key from your dashboard.

## Parameters

In our original release, API keys were included in the url. This worked extremely well - users could migrate to FireAcademy by just changing the base URL of their full nodes and removing certificate auth. We decided to keep this feature in the current release.

To use this method, just include your API key in the requested URL, between the domain and `leaflet`: `https://kraken.fireacademy.io/[api_key]/leaflet/[endpoint]`.

curl snippet:

```bash
curl https://kraken.fireacademy.io/1a7d0060-2d5a-473d-a8aa-a2cb0c277a31/leaflet/get_blockchain_state
```

## Headers

You can also include your API key as the value of a custom header, `X-API-Key`. Note that the header name is NOT case sensitive.

curl snipper:

```bash
curl -H 'X-API-Key: 1a7d0060-2d5a-473d-a8aa-a2cb0c277a31' https://kraken.fireacademy.io/leaflet/get_blockchain_state
```

## GET Query

Ironically, this method also works for POST requests. Just add an `api-key` query to the end of your request (`?api-key=YOUR-API-KEY`). Please note that the name is case-sensitive.

curl snipper:

```bash
curl -X POST 'https://kraken.fireacademy.io/leaflet/get_blockchain_state?api-key=1a7d0060-2d5a-473d-a8aa-a2cb0c277a31'
```
