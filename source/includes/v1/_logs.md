# Logs

Returns a your last 1,000 requests you made during the last 3 months.

```shell
curl --request GET \
  --url https://api.tomba.io/v1/logs \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx'
```

```php
<?php
use tomba\Tomba;

```

```python
import tomba

```

```javascript
const Tomba = require("tomba");
```

```ruby
require 'tomba'

```

```java
import io.tomba.api.Tomba;

```

```r
require(tomba)

```

```dart
import 'package:tomba/tomba.dart';

```

```powershell

```

### HTTP Request

`GET /logs/`

### Response Objects details

| Attribute              | Type   | Description                                |
| ---------------------- | ------ | ------------------------------------------ |
| `data` -> `uri`        | string | The url associated with the Request        |
| `data` -> `user_agent` | string | The User Agent associated with the Request |
| `data` -> `cost`       | bool   | The cost `false` Free `true` 1 request     |
| `data` -> `ip_address` | string | The IP address associated with the Request |
| `data` -> `created_at` | string | The date of creation                       |
| `data` -> `country`    | string | The ISO 3166-1 alpha-2 country code        |

> Full Response

```json
{
  "data": [
    {
      "type": "Email Finder",
      "uri": "https:\/\/api.tomba\/v1\/email-finder\/asdasd.fr",
      "cost": false,
      "ip_address": "1.0.0.0",
      "created_at": "2020-10-14T13:26:58+11:00",
      "id": 1809,
      "user_agent": "Mozilla\/5.0 (X11; Linux x86_64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/85.0.4183.121 Safari\/537.36",
      "source": "Website",
      "http_method": "GET",
      "country" : "TN"
    },
    {
      "type": "Social Search",
      "uri": "https:\/\/api.tomba\/v1\/social\/sadasd",
      "cost": false,
      "ip_address": "1.0.0.0",
      "created_at": "2020-10-14T13:26:35+11:00",
      "id": 1799,
      "user_agent": "Mozilla\/5.0 (X11; Linux x86_64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/85.0.4183.121 Safari\/537.36",
      "source": "Website",
      "http_method": "GET",
      "country" : "TN"
    },
    {
      "type": "Email Finder",
      "uri": "https:\/\/api.tomba\/v1\/email-finder\/alacra.com",
      "cost": false,
      "ip_address": "1.0.0.0",
      "created_at": "2020-10-14T00:22:13+11:00",
      "id": 1724,
      "user_agent": "Mozilla\/5.0 (X11; Linux x86_64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/85.0.4183.121 Safari\/537.36",
      "source": "Website",
      "http_method": "GET",
      "country" : "TN"
    },
    {
      "type": "Email Finder",
      "uri": "https:\/\/api.tomba\/v1\/email-finder\/alacra.com",
      "cost": false,
      "ip_address": "1.0.0.0",
      "created_at": "2020-10-14T00:22:01+11:00",
      "id": 1723,
      "user_agent": "Mozilla\/5.0 (X11; Linux x86_64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/85.0.4183.121 Safari\/537.36",
      "source": "Website",
      "http_method": "GET",
      "country" : "TN"
    },
    {
      "type": "Email Verification",
      "uri": "https:\/\/api.tomba\/v1\/email-verifier\/sdsad@asdsad.fr",
      "cost": true,
      "ip_address": "1.0.0.0",
      "created_at": "2020-10-12T22:07:03+11:00",
      "id": 1633,
      "user_agent": "Mozilla\/5.0 (X11; Linux x86_64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/85.0.4183.121 Safari\/537.36",
      "source": "Website",
      "http_method": "GET",
       "country" : "TN"
    },
    {
      "type": "Geolocation API",
      "uri": "https:\/\/api.tomba\/v1\/ip\/1.0.0.0",
      "cost": false,
      "ip_address": "1.0.0.0",
      "created_at": "2020-10-12T14:44:57+11:00",
      "id": 1290,
      "user_agent": "tomba api",
      "source": "API",
      "http_method": "GET",
       "country" : "TN"
    },
    {
      "type": "Email Verification",
      "uri": "https:\/\/api.tomba\/v1\/email-verifier\/asdasd@asdasd.fr",
      "cost": false,
      "ip_address": "1.0.0.0",
      "created_at": "2020-10-11T00:06:57+11:00",
      "id": 767,
      "user_agent": "Mozilla\/5.0 (X11; Linux x86_64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/85.0.4183.121 Safari\/537.36",
      "source": "Website",
      "http_method": "GET",
       "country" : "TN"
    },
    ...
    ...
    ...
    ...
    ...
    ...
  ]
}
```
