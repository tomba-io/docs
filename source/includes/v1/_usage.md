# Usage

Returns a your monthly requests

```shell
curl --request GET \
  --url https://api.tomba.io/v1/usage \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Usage;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$usage = new Usage($client);

$result = $usage->getUsage();

```

```python
from tomba.client import Client
from tomba.services.usage import Usage

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

usage = Usage(client)

result = usage.get_usage()

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let usage = new tomba.Usage(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = usage.getUsage();

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

usage = Tomba::Usage.new(client);

response = usage.get_usage();

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- usage(client)
data
```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Usage usage = Usage(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = usage.getUsage();

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

`GET /usage/`

### Response Objects details

| Attribute             | Type | Description             |
| --------------------- | ---- | ----------------------- |
| `data` ->`usage`      | int  | total usage on date     |
| `data` ->`created_at` | int  | usage date              |
| `data` ->`name`       | int  | total usage on the name |

> Full Response

```json
{
  "data": [
       {
      "usage": 2,
      "created_at": "2021-01-17",
      "domain": 0,
      "finder": 0,
      "verifier": 2,
      "technologies": 0,
      "ip": 0,
      "website": 0,
      "bulk": 0,
      "extension": 0,
      "api": 0,
      "mobile": 0,
      "desktop": 0,
      "sheets": 0
    },
    {
      "usage": 0,
      "created_at": "2021-01-19",
      "domain": 0,
      "finder": 0,
      "verifier": 0,
      "technologies": 0,
      "ip": 0,
      "website": 0,
      "bulk": 0,
      "extension": 0,
      "api": 0,
      "mobile": 0,
      "desktop": 0,
      "sheets": 0
    },
   ...
   ...
   ...
   ...
  ],
  "total": {
    "usage": 227,
    "domain": 0,
    "finder": 158,
    "verifier": 35,
    "technologies": 0,
    "website": 0,
    "bulk": 0,
    "extension": 0,
    "api": 0,
    "mobile": 0,
    "desktop": 0,
    "sheets": 0
  }
}
```
