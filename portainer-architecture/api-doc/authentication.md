---
description: Api authentication
---

# Authentication

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

