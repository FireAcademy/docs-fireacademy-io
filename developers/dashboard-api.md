# Dashboard API

The dashboard API can be accessed by anyone. Its source code can be found[ here](https://github.com/FireAcademy/data-dude/blob/master/dashboard\_api.go). Keep in mind that all requests need to have the `Authorization` header set to the Firebase authentication token of the user (no preceding `Bearer` ). All requests should use JSON encoding. The base URL for this API is `https://kraken.fireacademy.io/api`.



The following endpoints are exposed:

* `GET /stripe-dashboard-url` - Get the stripe dashboard URL for the logged in user.
* `GET /subscribe-url` - Get an URL that will allow the user to subscribe to a plan (given by the `plan_id` argument)
* `POST /user-plan` - Updates the user plan - upgrade or just switch auto-purchase of credit packages.
* `GET /dashboard-data` - Returns information about the user, their plan & API keys.
* `POST /api-key` - Creates an API key. Arguments: `name`, `origin`, `monthly_credit_limit`.
* `PUT /api-key` - Certainly a very good use for the `PUT` HTTP verb. Updates an existing API key. Takes the following arguments: `api_key`, `disabled`, `monthly_credit_limit`, `name`, `origin`.
* `POST /gift-code` - Redeems a gift code. Takes 2 arguments: `code` and `api_key`.
* `POST /ticket` - Creates a new ticket - intended for the 'Feedback and Ideas Form.' The endpoints expects 4 arguments: `message`, `emotional_state`, `anonymous`, and `contact`.
* `GET /updates` - Returns unread updates for the logged in user.
* `POST /updates` - Marks all updates as read.
* `GET /plans` - Returns a user's available plans, including custom ones.

``
