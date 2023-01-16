# Leaflet

The up-to-date source code for Leaflet can be found [here](https://github.com/fireacademy/leaflet). On a high level, Leaflet is just a proxy that takes incoming HTTP endpoints, 'wraps' them with the right certificates, sends them to the Chia full node, and returns the response. It also has a readiness check endpoint on `/ready`.

Any POST request to Leaflet's port (18444) will be treated as one that needs to be proxied to the Chia full node RPC.

## FireAcademy.io

Leaflet can be accessed at `https://kraken.fireacademy.io/leaflet/` or `https://kraken.fireacademy.io/{api-key}/leaflet/`. Each request has a different, static cost - please see [this page](../pricing.md) for more information, including a list of the allowed endpoints.
