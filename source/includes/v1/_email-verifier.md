# Email Verifier

This API endpoint allows you to verify the deliverability of an email address.

Tomba focuses on B2B. Therefore, webmails are not verified. We'll run every check but won't reach the remote SMTP server.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/email-verifier/ziad@test.io' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Verifier;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$verifier = new Verifier($client);

$result = $verifier->emailVerifier('b.mohamed@tomba.io');

```

```python
from tomba.client import Client
from tomba.services.verifier import Verifier

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

verifier = Verifier(client)

result = verifier.email_verifier('b.mohamed@tomba.io')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let verifier = new tomba.Verifier(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = verifier.emailVerifier('b.mohamed@tomba.io');

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

verifier = Tomba::Verifier.new(client);

response = verifier.email_verifier(email: 'b.mohamed@tomba.io');

puts response

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

## HTTP Request

`GET /email-verifier/:email`

### The parameters are defined as follows

| Parameter | Default  | Description                           |
| --------- | -------- | ------------------------------------- |
| `email`   | Required | The email address you want to verify. |

## Response  Objects details

> Full Response

```json
{
    "data": {
        "email": {
            "mx_records": true,
            "smtp_server": null,
            "smtp_check": true,
            "accept_all": null,
            "block": null,
            "email": "b.mohamed@tomba.io",
            "gibberish": false,
            "disposable": false,
            "webmail": false,
            "regex": true,
            "status": "valid",
            "result": "deliverable",
            "score": 82
        },
        "sources": [
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
}
```

| Attribute     | Type   | Description                                                                                                                                  |
| ------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `email`       | string | The email address to look up.                                                                                                                |
| `first_name`  | string | First name of person (if found)                                                                                                              |
| `last_name`   | string | Last name of person (if found)                                                                                                               |
| `country`     | string | Two letter country code based on location                                                                                                    |
| `mx_records`  | bool   | is `true` if we find MX records exist on the domain of the given email address.                                                              |
| `smtp_server` | bool   | is `true` if we connect to the SMTP server successfully.                                                                                     |
| `smtp_check`  | bool   | is `true` if the email address doesn't bounce.                                                                                               |
| `accept_all`  | bool   | is `true` if the SMTP server accepts all the email addresses. It means you can have have `false` positives on SMTP checks.                   |
| `block`       | bool   | is `true` if the SMTP server prevented us to perform the SMTP check.                                                                         |
| `score`       | int    | The deliverability score we give to the email address.                                                                                       |
| `regex`       | bool   | The email address passes our regular expression.                                                                                             |
| `full_name`   | string | The person's full name.                                                                                                                      |
| `status`      | string | returns the status of the email address. It takes 1 out of 6 possible values:`valid`,`invalid`,`accept_all`,`webmail`,`disposable`,`unknown` |
| `result`      | string | returns the main status of the verification. It takes 1 out of 3 possible values: `deliverable`,`undeliverable`,`risky`                      |
| `score`       | int    | is the deliverability score we give to the email address. For webmail and disposable emails, we provide an arbitrary score of 50.            |
| `source`      | array  | The given email address somewhere on the web                                                                                                 |
