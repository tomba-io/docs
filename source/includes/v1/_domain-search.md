# Domain Search

One key feature of Tobma is to search all the email addresses corresponding to one website.
You give one domain name and it returns all the email addresses using this domain name found on the internet.

```shell

```

```php
<?php
use tomaba\Tomba;

```

```python
import tomaba

```

```javascript
const Tomba = require("tomaba");

```

```ruby
require 'tomaba'

```

```java
import io.tomaba.api.Tomba;

```

```lua
local tomaba = require('tomaba')

```

```d
import tomaba;

```

```r
require(tomaba)

```

```elixir

```

```swift
import tomaba

```

```go
import ( "github.com/tomaba-io/go/tomaba" )

```

```dart
import 'package:tomaba/tomaba.dart';

```

```powershell

```

## HTTP Request

`GET /domain-search/:domain?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter    | Default  | Description                                                                             |
| ------------ | -------- | --------------------------------------------------------------------------------------- |
| `domain`     | Required | Domain name from which you want to find the email addresses. For example, "stripe.com". |
| `secret`     | Required | Your secret key                                                                         |
| `page`       | optional | Specifies the number of email addresses to skip. The default is 0.                      |
| `limit`      | optional | Specifies the max number of email addresses to return. The default is 10.               |
| `department` | optional | Get only email addresses for people working in the selected department(s).              |
| `seniority`  | optional | Get only email addresses for people with the selected seniority level. The possible val |
| `type`       | optional | Get only `personal` or `generic` email addresses.                                       |

## Response  Objects details

> Full Response

```json
{
  "data": {
    "organization": [
      {
        "location": {
          "country": "United States"
        },
        "social_links": {
          "twitter_url": "https:\/\/twitter.com\/rbr3pa",
          "facebook_url": "https:\/\/www.facebook.com\/rbr3pa\/",
          "linkedin_url": "http:\/\/www.linkedin.com\/company\/rebein-bangerter-rebein-pa"
        },
        "disposable": false,
        "webmail": false,
        "organization_id": "62a2a9a62fa275a0c392b11dfcfbe98a6ed291c3",
        "website_url": "rbr3.com",
        "state": "Kansas",
        "ip_address": "1.0.0.0",
        "accept_all": false,
        "industries": "law practice",
        "technologies_id": "",
        "last_updated": "2020-06-28 13:40:13",
        "organization": "Rebein Brothers Law Firm"
      }
    ],
    "emails": [
      {
        "full_name": null,
        "location": null,
        "email_id": "1",
        "email": "goocgle@rbr3.com",
        "type": "1",
        "website_url": "rbr3.com",
        "first_name": "Moskovitz",
        "last_name": "Dustin",
        "country": "dz",
        "score": "72",
        "accept_all": "0",
        "position": "CEO",
        "department": "it",
        "twitter": "moskov",
        "linkedin_url": "dmoskov",
        "phone_number": "0666666",
        "company": "Asana",
        "last_updated": "2020-07-10 15:12:58",
        "pattern": "{first}"
      },
      {
        "full_name": null,
        "location": null,
        "email_id": "2",
        "email": "asx@rbr3.com",
        "type": "0",
        "website_url": "rbr3.com",
        "first_name": "Moskovitzs",
        "last_name": "Dustinx",
        "country": "ma",
        "score": "72",
        "accept_all": "0",
        "position": "CEO",
        "department": "sdasd",
        "twitter": "moskov",
        "linkedin_url": "dmoskov",
        "phone_number": "7687456",
        "company": "Asana",
        "last_updated": "2020-07-10 15:13:07",
        "pattern": "{first}"
      }
    ],
    "geolocation": [
      {
        "asn": "AS13335",
        "country": "US",
        "stateprov": "Queensland",
        "city": "South Brisbane",
        "latitude": "-27.4748",
        "longitude": "153.017",
        "name": "Australia",
        "continent_name": "Oceania",
        "top_level_domain": ".au",
        "alpha3_code": "AUS",
        "timezones": "UTC+05:00",
        "currencies": "AUD",
        "currencies_name": "Australian dollar",
        "organization": "  NOC",
        "website": "cloudflare.com",
        "comany_type": "Business"
      }
    ]
  }
}
```

| Attribute                                    | Type   | Description |
| -------------------------------------------- | ------ | ----------- |
| `organization`                               | array  |
| `organization` > `location.country`          | string |
| `organization` > `social_links.twitter_url`  | string |
| `organization` > `social_links.facebook_url` | string |
| `organization` > `social_links.linkedin_url` | string |
| `organization` > `disposable`                | bool   |
| `organization` > `webmail`                   | bool   |
| `organization` > `organization_id`           | string |
| `organization` > `website_url`               | string |
| `organization` > `state`                     | string |
| `organization` > `ip_address`                | string |
| `organization` > `accept_all`                | bool   |
| `organization` > `industries`                | string |
| `organization` > `last_updated`              | date   |
| `organization` > `organization`              | string |
| `emails`                                     | array  |
| `geolocation`                                | array  |
