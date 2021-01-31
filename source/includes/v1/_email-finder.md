# Email Finder

This API endpoint generates or retrieves the most likely email address from a domain name, a first name and a last name.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/email-finder/asana.com?first_name=Moskoz&last_name=Dustin' \
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

`GET /email-finder/:domain`

### The parameters are defined as follows

| Parameter  | Default  | Description                                                                |
| ---------- | -------- | -------------------------------------------------------------------------- |
| domain     | Required | The domain name of the company, used for emails. For example, "asana.com". |
| full_name  | Required | The person's full name                                                     |
| first_name | Required | The person's first name. It doesn't need to be in lowercase..              |
| last_name  | Required | The person's last name. It doesn't need to be in lowercase..               |

## Response Objects details

> Full Response

```json
{
  "data": {
    "email": [
      {
        "email": "googxle@asana.com",
        "type": "1",
        "website_url": "asana.com",
        "first_name": "Moskoz",
        "last_name": "Dustin",
        "country": "tr",
        "score": 72,
        "accept_all": false,
        "position": "CEO",
        "department": "ascsd",
        "twitter": "moskov",
        "linkedin_url": "dmoskov",
        "phone_number": "5646456",
        "company": "Asana",
        "latitude": "0",
        "longitude": "0",
        "last_updated": "2020-08-19 13:58:19",
        "full_name": "Moskoz Dustin"
      }
    ],
    "sources": false
  }
}
```

| Attribute      | Type   | Description                                                                                                                |
| -------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `email`        | string | The email address                                                                                                          |
| `type`         | string | Get the count of only personal or generic email addresses.                                                                 |
| `website_url`  | string | Company domain                                                                                                             |
| `first_name`   | string | First name of person (if found)                                                                                            |
| `last_name`    | string | Last name of person (if found)                                                                                             |
| `full_name`    | string | Full formatted name of person. Sometimes this will be present even if the `last_name` or `first_name` aren’t available     |
| `country`      | string | Two letter country code based on location                                                                                  |
| `accept_all`   | bool   | is `true` if the SMTP server accepts all the email addresses. It means you can have have `false` positives on SMTP checks. |
| `position`     | string | The job title of person (if found)                                                                                         |
| `department`   | string | The person working in the selected department(s).                                                                          |
| `twitter`      | string | Twitter handle for the person (if found).                                                                                  |
| `linkedin_url` | string | LinkedIn URL for the person (if found).                                                                                    |
| `phone_number` | string | The phone number of person (if found)                                                                                      |
| `company`      | string | The company of person (if found)                                                                                           |
| `latitude`     | string | latitude based on location                                                                                                 |
| `longitude`    | string | longitude based on location                                                                                                |
| `last_updated` | string | The time at which we update this data                                                                                      |
