# Logs

Returns a your last 1,000 requests you made during the last 3 months.

```shell
curl --request GET \
  --url https://api.tomba.io/v1/logs \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Logs;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$logs = new Logs($client);

$result = $logs->getLogs();

```

```python
from tomba.client import Client
from tomba.services.logs import Logs

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

logs = Logs(client)

result = logs.get_logs()

```

```javascript
const tomba = require("tomba");

// Init Tomba
let client = new tomba.Client();

let logs = new tomba.Logs(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
let result = logs.getLogs();

result
  .then((response) => {
    console.log(response);
  })
  .catch((err) => {
    console.log(err);
  });
```

```ruby
require 'tomba'

client = Tomba::Client.new()

client
    .set_key('ta_xxxx') # Your Key
    .set_secret('ts_xxxx') # Your Secret
;

logs = Tomba::Logs.new(client);

response = logs.get_logs();

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- logs(client)
data

```

```dart
import 'package:tomba/tomba.dart';

void main() {
  // Init SDK
  Client client = Client();
  Logs logs = Logs(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = logs.getLogs();

  result
    .then((response) {
      print(response);
    }).catchError((error) {
      print(error.response);
  });
}
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
