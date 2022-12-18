---
description: The Beta API is in... beta.
---

# Beta API

## Puzzles

Wondering what's hidden behind an inner puzzle hash? Use this endpoint!

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
