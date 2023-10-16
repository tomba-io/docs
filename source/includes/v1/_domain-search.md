# Domain Search

Search emails are based on the website
You give one domain name and it returns all the email addresses found on the internet.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/domain-search?domain=stripe.com' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Domain;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$domain = new Domain($client);

$result = $domain->domainSearch('stripe.com');

```

```python
from tomba.client import Client
from tomba.services.domain import Domain

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

domain = Domain(client)

result = domain.domain_search('stripe.com')

```

```javascript
const tomba = require("tomba");

// Init Tomba
let client = new tomba.Client();

let domain = new tomba.Domain(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
let result = domain.domainSearch("stripe.com");

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

domain = Tomba::Domain.new(client);

response = domain.domain_search(domain: 'stripe.com');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- domain_search(client, domain="tomba.io")
data

```

```dart
import 'package:tomba/tomba.dart';

void main() {
  // Init SDK
  Client client = Client();
  Domain domain = Domain(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = domain.domainSearch(
    domain: 'stripe.com',
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

`GET /domain-search/?domain=:domain`

### The parameters are defined as follows

| Parameter    | Default  | Description                                                                                            |
| ------------ | -------- | ------------------------------------------------------------------------------------------------------ |
| `domain`     | Required | Domain name from which you want to find the email addresses. For example, "stripe.com".                |
| `page`       | optional | Specifies the number of email addresses to skip. The default is `1`.                                   |
| `limit`      | optional | Specifies the max number of email addresses to return. The default is 10. valid number(`10`,`20`,`50`) |
| `department` | optional | Get only email addresses for people working in the selected department(s).                             |
| `type`       | optional | Get only `personal` or `generic` email addresses.                                                      |

## Response Objects details

> Full Response

```json
{
    "data": {
        "organization": {
            "location": {
                "country": "US",
                "city": "San Francisco",
                "state": "California",
                "street_address": "-122.41",
                "postal_code": "94107"
            },
            "social_links": {
                "twitter_url": "https://twitter.com/stripe",
                "facebook_url": "https://www.facebook.com/StripeHQ",
                "linkedin_url": "https://www.linkedin.com/company/2135371"
            },
            "disposable": false,
            "webmail": false,
            "website_url": "stripe.com",
            "phone_number": "",
            "industries": "internet",
            "founded": "2010",
            "company_size": "1001-5000",
            "last_updated": "2023-10-14T15:02:33+02:00",
            "accept_all": true,
            "description": "Stripe is a financial infrastructure platform for businesses. Millions of companies—from the world’s largest enterprises to the most ambitious startups—use Stripe to accept payments, grow their revenue, and accelerate new business opportunities. Headquartered in San Francisco and Dublin, the company aims to increase the GDP of the internet.",
            "pattern": "{first}",
            "organization": "stripe",
            "whois": {
                "registrar_name": "SafeNames Ltd.",
                "created_date": "1995-09-12T06:00:00+02:00",
                "referral_url": "http://www.safenames.net"
            }
        },
        "emails": [
            {
                "email": "**@stripe.com",
                "first_name": "***",
                "last_name": "**",
                "full_name": "*** ***",
                "gender": "female",
                "phone_number": false,
                "type": "generic",
                "country": "US",
                "position": "Financial Crimes Analyst",
                "department": "finance",
                "seniority": "senior",
                "twitter": null,
                "linkedin": "https://www.linkedin.com/in/*****",
                "score": 55,
                "verification": {
                    "date": null,
                    "status": null
                },
                "sources": [
                    {
                        "uri": "https://stripe.com/docs/cli",
                        "website_url": "stripe.com",
                        "extracted_on": "2022-03-08T01:23:16+01:00",
                        "last_seen_on": "2022-08-04T09:42:10+02:00",
                        "still_on_page": true
                    }
                ]
            }
            ...
            ...
        ]
    },
    "meta": {
        "total": 2079,
        "pageSize": 10,
        "current": 1,
        "total_pages": 207,
        "params": {
            "domain": "stripe.com",
            "page": 1,
            "limit": 10,
            "department": "",
            "type": "all"
        }
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
