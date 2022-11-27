# Creating an API Key

API keys can be created by pressing the 'Generate' button of the 'API Keys' section in the [FireAcademy.io Dashboard](https://dashboard.fireacademy.io). When creating an API key, you will be asked for 3 things:

## Name

The name is something that is only visible to you. It is intended to help you distinguish between different API keys. To avoid confusion, it is recommended that you use a highly suggestive name.

## Origin

This is a [CORS](https://en.wikipedia.org/wiki/Cross-origin\_resource\_sharing)-related parameter. Default is `*`.

## Weekly Credit Limit

Through this parameter, you can control how many credits an API key is allowed to use each week. API keys whose usage reached this limit will be considered invalid until the next week. Default is 0, which means that the key has no weekly credit limit.

