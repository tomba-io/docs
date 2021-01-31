# Domain Search

Search emails are based on the website
You give one domain name and it returns all the email addresses found on the internet.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/domain-search/google.com' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx' \
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

`GET /domain-search/:domain`

### The parameters are defined as follows

| Parameter    | Default  | Description                                                                             |
| ------------ | -------- | --------------------------------------------------------------------------------------- |
| `domain`     | Required | Domain name from which you want to find the email addresses. For example, "stripe.com". |
| `page`       | optional | Specifies the number of email addresses to skip. The default is 1.                      |
| `limit`      | optional | Specifies the max number of email addresses to return. The default is 10.               |
| `department` | optional | Get only email addresses for people working in the selected department(s).              |
| `seniority`  | optional | Get only email addresses for people with the selected seniority level. The possible val |
| `type`       | optional | Get only `personal` or `generic` email addresses.                                       |

## Response Objects details

> Full Response

```json
{
  "data": {
    "organization": [
      {
        "location": {
          "country": null
        },
        "social_links": {
          "twitter_url": null,
          "facebook_url": null,
          "linkedin_url": null
        },
        "disposable": false,
        "webmail": false,
        "website_url": "google.com",
        "state": null,
        "employee_count": 0,
        "last_updated": "2021-01-30T16:25:48+01:00",
        "revenue": null,
        "city": null,
        "accept_all": false,
        "pattern": "{first}",
        "organization": "Google"
      }
    ],
    "emails": [
      {
        "email": "xxx@google.com",
        "first_name": null,
        "last_name": null,
        "full_name": null,
        "phone_number": null,
        "type": "generic",
        "country": null,
        "position": "",
        "department": "executive",
        "seniority": null,
        "twitter": null,
        "linkedin": null,
        "accept_all": false,
        "score": 95,
        "verification": {
          "date": null,
          "status": null
        },
        "last_updated": "2021-01-31T12:41:00+01:00",
        "sources": [
          {
            "uri": "http:\/\/betterthanstockcars.com\/",
            "extracted_on": "2020-11-10 03:23:53",
            "last_seen_on": "2021-01-31 12:41:00",
            "still_on_page": true,
            "website_url": "betterthanstockcars.com"
          },
          {
            "uri": "http:\/\/departamentuldecontabilitate.ro\/",
            "extracted_on": "2020-11-08 18:52:14",
            "last_seen_on": "2021-01-31 12:46:50",
            "still_on_page": true,
            "website_url": "departamentuldecontabilitate.ro"
          },
          {
            "uri": "http:\/\/departamentuldecontabilitate.ro\/servicii\/analiza-financiara\/",
            "extracted_on": "2020-11-08 18:52:14",
            "last_seen_on": "2021-01-31 12:46:50",
            "still_on_page": true,
            "website_url": "departamentuldecontabilitate.ro"
          }
        ]
      },
      {
        "email": "xxx@google.com",
        "first_name": null,
        "last_name": null,
        "full_name": null,
        "phone_number": null,
        "type": "personal",
        "country": null,
        "position": null,
        "department": null,
        "seniority": null,
        "twitter": null,
        "linkedin": null,
        "accept_all": false,
        "score": 95,
        "verification": {
          "date": null,
          "status": null
        },
        "last_updated": "2021-01-31T12:45:18+01:00",
        "sources": [
          {
            "uri": "http:\/\/community.apache.org\/gsoc-admin-tasks.html",
            "extracted_on": "2020-11-04 23:36:07",
            "last_seen_on": "2021-01-31 12:45:18",
            "still_on_page": true,
            "website_url": "community.apache.org"
          }
        ]
      },
      {
        "email": "xxx@google.com",
        "first_name": null,
        "last_name": null,
        "full_name": null,
        "phone_number": null,
        "type": "personal",
        "country": null,
        "position": null,
        "department": null,
        "seniority": null,
        "twitter": null,
        "linkedin": null,
        "accept_all": false,
        "score": 95,
        "verification": {
          "date": null,
          "status": null
        },
        "last_updated": "2021-01-31T12:45:18+01:00",
        "sources": [
          {
            "uri": "http:\/\/community.apache.org\/gsoc-admin-tasks.html",
            "extracted_on": "2020-11-04 23:36:07",
            "last_seen_on": "2021-01-31 12:45:18",
            "still_on_page": true,
            "website_url": "community.apache.org"
          }
        ]
      },
      ...
      ...
      ...
    ]
  },
  "meta": {
    "total": 336,
    "pageSize": 10,
    "current": 0,
    "total_pages": 34
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
| `organization` > `website_url`               | string | The Domain of company’s website       |
| `organization` > `state`                     | string | The company state                     |
| `organization` > `accept_all`                | bool   | The SMTP checks                       |
| `organization` > `industries`                | string | The company industries info           |
| `organization` > `last_updated`              | date   | The time at which we update this data |
| `organization` > `organization`              | string | The Name of company                   |
| `organization` > `pattern`                   | string | The Name of company                   |
| `emails`                                     | array  | The list of Emails                    |
