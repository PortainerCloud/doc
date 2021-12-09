---
description: Api authentication
---

# Authentication

## Request

{% tabs %}
{% tab title="cURL" %}
```text
curl -XPOST 'https://authapi.portainer.cloud/oauth/token' \
--header 'Content-Type: application/json' \
--data-raw '{
  "username": "my@email.com",
  "password": "my@password"
}'
```
{% endtab %}
{% endtabs %}

use your credential to authenticate and get a jwt from the authentication service.

## Response

{% tabs %}
{% tab title="403" %}
```json
{"error":"invalid_grant","error_description":"Wrong email or password."}
```
{% endtab %}
{% tab title="201" %}
```json
{"error":"invalid_grant","error_description":"Wrong email or password."}
```
{% endtab %}
{% endtabs %}
