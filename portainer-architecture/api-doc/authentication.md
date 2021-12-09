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
{% tab title="201" %}
```json
{
  "token":"ey...-uPSw",
  "created_at":"2021-12-09T13:57:15.358Z"
}
```
{% endtab %}
{% tab title="403" %}
```json
{
  "error":"invalid_grant",
  "error_description":"Wrong email or password."
}
```
{% endtab %}
{% tab title="429" %}
```json
{
  "error":"too_many_attempts",
  "error_description":"Your account has been blocked after multiple consecutive login attempts. We've sent you an email with instructions on how to unblock it."
}
```
{% endtab %}
{% endtabs %}
