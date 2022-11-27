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

## Parameters

aaa

## Headers

aaaa

## GET Query

aaa
