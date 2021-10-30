# Autocomplete

Company Autocomplete is an API that lets you auto-complete company names and retrieve logo and domain information.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/domains-suggestion?query=googl' \
  --header 'Content-Type: application/json' \
```

```php
use Tomba\Client;
use Tomba\Services\Status;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$status = new Status($client);

$result = $status->autoComplete('google');

```

```python
from tomba.client import Client
from tomba.services.status import Status

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

status = Status(client)

result = status.auto_complete('google')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let status = new tomba.Status(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = status.autoComplete('google');

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

status = Tomba::Status.new(client);

response = status.auto_complete(query: 'google');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- autocomplete(client, search="to")
data

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Status status = Status(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = status.autoComplete(
    query: 'google',
  );

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

`GET /domains-suggestion?query=:query`

### The parameters are defined as follows

| Parameter | Default  | Description                     |
| --------- | -------- | ------------------------------- |
| query     | Required | name of the company or website. |

### Response Objects details

| Attribute               | Type   | Description            |
| ----------------------- | ------ | ---------------------- |
| `data` -> `email_count` | int    | Total email on company |
| `data` -> `website_url` | string | Domain website         |
| `data` -> `name`        | string | Domain name of company |
| `data` -> `logo`        | string | URL to logo            |

> Full Response

```json
{
  "data": [
    {
      "website_url": "google.com",
      "name": "Google",
      "email_count": 336,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=google.com"
    },
    {
      "website_url": "txt.voice.google.com",
      "name": "Txt",
      "email_count": 2,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=txt.voice.google.com"
    },
    {
      "website_url": "googlegroups.com",
      "name": "Googlegroups",
      "email_count": 5,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=googlegroups.com"
    },
    {
      "website_url": "ooglesngoogles.com",
      "name": "Ooglesngoogles",
      "email_count": 1,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=ooglesngoogles.com"
    },
    {
      "website_url": "googlemail.con",
      "name": "Googlemail",
      "email_count": 2,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=googlemail.con"
    }
  ],
  "meta": {
    "limit": null,
    "query": "googl"
  }
}
```
