# Email Sources

Find email address source somewhere on the web  

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/email-sources/b.mohamed@tomba.io' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ts_xxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Sources;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$sources = new Sources($client);

$result = $sources->emailSources('b.mohamed@tomba.io');

```

```python
from tomba.client import Client
from tomba.services.sources import Sources

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

sources = Sources(client)

result = sources.email_sources('b.mohamed@tomba.io')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let sources = new tomba.Sources(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = sources.emailSources('b.mohamed@tomba.io');

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

sources = Tomba::Sources.new(client);

response = sources.email_sources(email: 'b.mohamed@tomba.io');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- email_sources(client, email="b.mohamed@tomba.io")
data

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Sources sources = Sources(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = sources.emailSources(
    email: 'b.mohamed@tomba.io',
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

## HTTP Request

`GET /email-sources/:email`

### The parameters are defined as follows

| Parameter | Default  | Description                                 |
| --------- | -------- | ------------------------------------------- |
| `email`   | Required | The email address you want to find sources. |

## Response  Objects details

> Full Response

```json
{
    "email": "b.mohamed@tomba.io",
    "data": [
        {
            "uri": "https:\/\/github.com\/tomba-io\/generic-emails\/blob\/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9\/src\/lib\/validation\/hash.ts",
            "extracted_on": "2021-02-08T20:09:54+01:00",
            "last_seen_on": "2021-02-08T22:43:40+01:00",
            "still_on_page": true,
            "website_url": "github.com"
        },
        {
            "uri": "https:\/\/github.com\/tomba-io\/generic-emails\/blame\/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9\/src\/lib\/validation\/hash.ts",
            "extracted_on": "2021-02-08T20:09:59+01:00",
            "last_seen_on": "2021-02-08T22:43:40+01:00",
            "still_on_page": true,
            "website_url": "github.com"
        }
    ]
}
```

| Attribute | Type   | Description                                  |
| --------- | ------ | -------------------------------------------- |
| `email`   | string | The email address to look up.                |
| `source`  | array  | The given email address somewhere on the web |
