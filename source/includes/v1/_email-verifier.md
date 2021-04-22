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
            "score": 80
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

| Attribute     | Type   | Description                                                                                                                |
| ------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `email`       | string | The email address to look up.                                                                                              |
| `first_name`  | string | First name of person (if found)                                                                                            |
| `last_name`   | string | Last name of person (if found)                                                                                             |
| `country`     | string | Two letter country code based on location                                                                                  |
| `mx_records`  | bool   | is `true` if we find MX records exist on the domain of the given email address.                                            |
| `smtp_server` | bool   | is `true` if we connect to the SMTP server successfully.                                                                   |
| `smtp_check`  | bool   | is `true` if the email address doesn't bounce.                                                                             |
| `accept_all`  | bool   | is `true` if the SMTP server accepts all the email addresses. It means you can have have `false` positives on SMTP checks. |
| `block`       | bool   | is `true` if the SMTP server prevented us to perform the SMTP check.                                                       |
| `score`       | int    | The deliverability score we give to the email address.                                                                     |
| `regex`       | bool   | The email address passes our regular expression.                                                                           |
| `full_name`   | string | The person's full name.                                                                                                    |
| `source`      | array  | The given email address somewhere on the web                                                                               |
