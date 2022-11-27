# Dashboard API

The dashboard API can be accessed by anyone. Its source code can be found [here](https://github.com/FireAcademy/catchpole/blob/master/dashboard\_api.go). Keep in mind that all requests need to have the `Authorization` header set to the Firebase authentication token of the user (no preceding `Bearer` ). All requests should use JSON encoding. The base URL for this api is `https://kraken.fireacademy.io`.



The following endpoints are exposed:

* `GET /api/stripe-url` - Get the stripe dashboard URL (or checkout URL, if the user is not susbcribed to our service) for the logged in user.
* `GET /api/dashboard-data` - Get dashboard data for the logged in user (details about the user and API keys).
* `POST /api/api-key` - Creates an API key. Takes 3 arguments: `weekly_credit_limit`, `name`, `origin`.
* `PUT /api/api-key` - Certianly a very good use for the `PUT` HTTP verb. Updates an existing API key. Takes the following arguments: `api_key`, `disabled`, `weekly_credit_limit`, `name`, `origin`.
* `POST /gift-code` - Reedeems a gift code. Takes 2 arguments: `code` and `api_key`.
