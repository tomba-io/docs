# Email Verifier

This API endpoint allows you to verify the deliverability of an email address.

Tomba focuses on B2B. Therefore, Webmail are not verified. We'll run every check but won't reach the remote SMTP server.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/email-verifier/b.mohamed@tomba.io' \
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
const tomba = require("tomba");

// Init Tomba
let client = new tomba.Client();

let verifier = new tomba.Verifier(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
let result = verifier.emailVerifier("b.mohamed@tomba.io");

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
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- email_verifier(client, email="b.mohamed@tomba.io")
data

```

```dart
import 'package:tomba/tomba.dart';

void main() {
  // Init SDK
  Client client = Client();
  Verifier verifier = Verifier(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = verifier.emailVerifier(
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

`GET /email-verifier/:email`

### The parameters are defined as follows

| Parameter | Default  | Description                           |
| --------- | -------- | ------------------------------------- |
| `email`   | Required | The email address you want to verify. |

## Response Objects details

> Full Response

```json
{
  "data": {
    "email": {
      "mx_records": true,
      "smtp_server": true,
      "smtp_check": true,
      "accept_all": false,
      "block": false,
      "email": "b.mohamed@tomba.io",
      "gibberish": false,
      "disposable": false,
      "webmail": false,
      "regex": true,
      "whois": {
        "registrar_name": "NameCheap, Inc.",
        "created_date": "2020-07-07 20:54:07",
        "referral_url": "https://www.namecheap.com/"
      },
      "status": "valid",
      "result": "deliverable",
      "score": 100
    },
    "sources": [
      {
        "uri": "https://github.com/tomba-io/generic-emails/blob/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9/src/lib/validation/hash.ts",
        "website_url": "github.com",
        "extracted_on": "2021-02-08T20:09:54+01:00",
        "last_seen_on": "2021-02-08T22:43:40+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://github.com/tomba-io/generic-emails/blame/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9/src/lib/validation/hash.ts",
        "website_url": "github.com",
        "extracted_on": "2021-02-08T20:09:59+01:00",
        "last_seen_on": "2021-02-08T22:43:40+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://katta.co/tomba-review/",
        "website_url": "katta.co",
        "extracted_on": "2021-06-02T13:41:50+02:00",
        "last_seen_on": "2021-06-02T18:26:12+02:00",
        "still_on_page": true
      },
      {
        "uri": "https://shards.info/github/benemohamed/",
        "website_url": "shards.info",
        "extracted_on": "2021-10-26T15:36:04+02:00",
        "last_seen_on": "2021-12-22T23:57:50+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://githubmemory.com/repo/tomba-io/python",
        "website_url": "githubmemory.com",
        "extracted_on": "2021-10-26T15:36:37+02:00",
        "last_seen_on": "2021-12-22T23:57:49+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://pypi.org/project/tomba-io/",
        "website_url": "pypi.org",
        "extracted_on": "2021-10-26T15:37:41+02:00",
        "last_seen_on": "2021-10-26T15:37:46+02:00",
        "still_on_page": true
      },
      {
        "uri": "https://www.npmjs.com/package/tomba",
        "website_url": "www.npmjs.com",
        "extracted_on": "2021-10-26T15:39:28+02:00",
        "last_seen_on": "2021-10-26T15:39:36+02:00",
        "still_on_page": true
      },
      {
        "uri": "https://cnpmjs.org/package/tomba",
        "website_url": "cnpmjs.org",
        "extracted_on": "2021-10-26T18:58:53+02:00",
        "last_seen_on": "2021-12-22T23:58:49+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://packosphere.com/tombaio/tomba-meteor",
        "website_url": "packosphere.com",
        "extracted_on": "2021-10-28T00:52:33+02:00",
        "last_seen_on": "2021-12-23T00:02:43+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://www.pkgstats.com/pkg:tomba",
        "website_url": "www.pkgstats.com",
        "extracted_on": "2021-10-28T00:53:39+02:00",
        "last_seen_on": "2021-10-28T00:53:44+02:00",
        "still_on_page": true
      },
      {
        "uri": "https://pub.dev/packages/tomba",
        "website_url": "pub.dev",
        "extracted_on": "2021-10-30T15:28:18+02:00",
        "last_seen_on": "2021-10-30T15:28:45+02:00",
        "still_on_page": true
      },
      {
        "uri": "https://pub.dev/packages/tomba/license",
        "website_url": "pub.dev",
        "extracted_on": "2021-10-30T15:28:19+02:00",
        "last_seen_on": "2021-10-30T15:28:45+02:00",
        "still_on_page": true
      },
      {
        "uri": "https://pub.dev/packages/tomba/versions/1.0.0",
        "website_url": "pub.dev",
        "extracted_on": "2021-10-30T15:28:25+02:00",
        "last_seen_on": "2021-10-30T15:28:47+02:00",
        "still_on_page": true
      },
      {
        "uri": "https://cnpmjs.org/package/tomba/v/1.0.0",
        "website_url": "cnpmjs.org",
        "extracted_on": "2021-12-22T14:21:30+01:00",
        "last_seen_on": "2021-12-22T23:58:49+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://r.cnpmjs.org/tomba",
        "website_url": "r.cnpmjs.org",
        "extracted_on": "2021-12-22T14:23:16+01:00",
        "last_seen_on": "2021-12-22T23:58:51+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://github.com/tomba-io/r",
        "website_url": "github.com",
        "extracted_on": "2021-12-22T14:41:25+01:00",
        "last_seen_on": "2021-12-23T00:02:09+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://rdrr.io/cran/tomba/f/README.md",
        "website_url": "rdrr.io",
        "extracted_on": "2021-12-22T14:41:37+01:00",
        "last_seen_on": "2021-12-23T00:02:18+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://packosphere.com/tombaio/tomba-meteor/1.0.0",
        "website_url": "packosphere.com",
        "extracted_on": "2021-12-22T14:42:21+01:00",
        "last_seen_on": "2021-12-23T00:02:43+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://githubmemory.com/repo/tomba-io/node",
        "website_url": "githubmemory.com",
        "extracted_on": "2021-12-22T15:44:03+01:00",
        "last_seen_on": "2021-12-23T00:10:51+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://www.nuget.org/packages/Tomba/1.0.0",
        "website_url": "www.nuget.org",
        "extracted_on": "2021-12-22T15:44:25+01:00",
        "last_seen_on": "2021-12-23T00:10:52+01:00",
        "still_on_page": true
      }
    ]
  }
}
```

| Attribute     | Type   | Description                                                                                                                                  |
| ------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `email`       | string | The email address to look up.                                                                                                                |
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
