---
description: The Beta API is in... beta.
---

# Beta API

For a better experience, please refer to [this generated page](https://app.swaggerhub.com/apis-docs/Yakuhito/BetaAPI/1.0).

## Puzzles

Wondering what's hidden behind a singleton's inner puzzle hash? Use this endpoint to find out!

{% swagger src="../.gitbook/assets/swagger.yaml" path="/get_puzzle" method="post" %}
[swagger.yaml](../.gitbook/assets/swagger.yaml)
{% endswagger %}

## Singleton States

The reason Beta was invented.

{% swagger src="../.gitbook/assets/swagger.yaml" path="/get_singleton_states" method="post" %}
[swagger.yaml](../.gitbook/assets/swagger.yaml)
{% endswagger %}

## Sync

Is Beta up-to-date or a trillion blocks behind?

**Warning**: Not suitable for heptapods.

{% swagger src="../.gitbook/assets/swagger.yaml" path="/get_peak_synced_block" method="get" %}
[swagger.yaml](../.gitbook/assets/swagger.yaml)
{% endswagger %}

{% swagger src="../.gitbook/assets/swagger.yaml" path="/get_peak_synced_block" method="post" %}
[swagger.yaml](../.gitbook/assets/swagger.yaml)
{% endswagger %}

{% swagger src="../.gitbook/assets/swagger.yaml" path="/get_synced_block" method="post" %}
[swagger.yaml](../.gitbook/assets/swagger.yaml)
{% endswagger %}

{% swagger src="../.gitbook/assets/swagger.yaml" path="/get_synced_blocks" method="post" %}
[swagger.yaml](../.gitbook/assets/swagger.yaml)
{% endswagger %}
