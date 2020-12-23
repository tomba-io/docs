# Domain Search

One key feature of Tobma is to search all the email addresses corresponding to one website.
You give one domain name and it returns all the email addresses using this domain name found on the internet.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/domain-search/rbr3.com' \
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

`GET /domain-search/:domain`

### The parameters are defined as follows

| Parameter    | Default  | Description                                                                             |
| ------------ | -------- | --------------------------------------------------------------------------------------- |
| `domain`     | Required | Domain name from which you want to find the email addresses. For example, "stripe.com". |
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

| Attribute                                    | Type   | Description                           |
| -------------------------------------------- | ------ | ------------------------------------- |
| `organization` > `location.country`          | string | The country of company                |
| `organization` > `social_links.twitter_url`  | string | The Twitter screen name               |
| `organization` > `social_links.facebook_url` | string | The Facebook screen name              |
| `organization` > `social_links.linkedin_url` | string | The Linkedin screen name              |
| `organization` > `disposable`                | bool   | is disposable email service           |
| `organization` > `webmail`                   | bool   | is webmail email                      |
| `organization` > `organization_id`           | hash   | Internal ID                           |
| `organization` > `website_url`               | string | The Domain of company’s website       |
| `organization` > `state`                     | string | The company state                     |
| `organization` > `ip_address`                | string | The IP of company                     |
| `organization` > `accept_all`                | bool   | The SMTP checks                       |
| `organization` > `industries`                | string | The company industries info           |
| `organization` > `last_updated`              | date   | The time at which we update this data |
| `organization` > `organization`              | string | The Name of company                   |
| `emails`                                     | array  | The list of Emails                    |
| `geolocation`                                | array  | The company geolocation info          |
