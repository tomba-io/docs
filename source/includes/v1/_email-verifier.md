# Email Verifier

This API endpoint allows you to verify the deliverability of an email address.

Tomba focuses on B2B. Therefore, webmails are not verified. We'll run every check but won't reach the remote SMTP server.

This endpoint is rate-limited by domain name. You can check up to 200 email addresses for a domain name every 24 hours. You can check the number of requests remaining using the X-RateLimit-Remaining header.

The request will run for 20 seconds. If it was not able to provide a response in time, we will return a 202 status code. You will then be able to poll the same endpoint to get the verification's result. Of course, all the requests in this case are counted only once.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/email-verifier/ziad@test.io' \
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
    "email": [
      {
        "email_id": "85136c79cbf9fe36bb9d05d0639c70c265c18d37%5",
        "email": "ziad@test.io",
        "first_name": "asd",
        "last_name": "asd",
        "country": "dz",
        "mx_records": true,
        "smtp_server": true,
        "smtp_check": true,
        "accept_all": false,
        "block": true,
        "score": 22,
        "regex": true,
        "full_name": "asd asd"
      }
    ],
    "sources": [
      {
        "website_url": "test.io",
        "uri": "https:\/\/www.youtube.com\/",
        "extracted_on": "2020-05-17",
        "last_seen_on": "2020-05-17",
        "still_on_page": false
      },
      {
        "website_url": "test.io",
        "uri": "https:\/\/www.facebook.com\/",
        "extracted_on": "2020-05-17",
        "last_seen_on": "2020-05-17",
        "still_on_page": true
      },
      ...
      ...
      ...
      ...
    ]
  }
}
```

| Attribute     | Type   | Description                                                                                                                |
| ------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `email_id`    | hash   | Internal ID                                                                                                                |
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
