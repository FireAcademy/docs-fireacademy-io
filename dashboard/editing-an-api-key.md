# Editing an API Key

API keys can be modified by pressing 'Modify' in the corresponding entry in the 'API Keys' section of the [FireAcademy.io Dashboard](https://dashboard.fireacademy.io). When modifying an API key, you will be allowed to change 4 fields:

## Name

The name is something that is only visible to you. It is intended to help you distinguish between different API keys. To avoid confusion, it is highly recommended that you use a highly suggestive name.

## Origin

This is a [CORS](https://en.wikipedia.org/wiki/Cross-origin\_resource\_sharing)-related parameter. Default is `*`.

## Weekly Credit Limit

Through this parameter, you can control how many credits an API key is allowed to use each week. API keys whose usage reached this limit will be considered invalid until the next week. Default is 0, which means that the key has no weekly credit limit.

## Status

If you would like to invalidate an API key (the closest you can get to deleting it), you can set the status to 'Disabled'. This will cause catchpole to reject all requests that use the given key.
