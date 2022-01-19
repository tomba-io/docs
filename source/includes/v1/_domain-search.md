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
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let domain = new tomba.Domain(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = domain.domainSearch('stripe.com');

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
| `page`       | optional | Specifies the number of email addresses to skip. The default is `1`.                                     |
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
                "street_address": null
            },
            "social_links": {
                "twitter_url": "https:\/\/twitter.com\/stripe",
                "facebook_url": "https:\/\/www.facebook.com\/StripeHQ",
                "linkedin_url": "https:\/\/www.linkedin.com\/company\/2135371"
            },
            "disposable": false,
            "webmail": false,
            "website_url": "stripe.com",
            "phone_number": "",
            "industries": "internet",
            "postal_code": "94107",
            "employee_count": 976,
            "last_updated": "2021-01-09T05:51:19+01:00",
            "revenue": "150000",
            "accept_all": false,
            "pattern": "{first}",
            "domain_score": 30,
            "organization": "stripe"
        },
        "emails": [
            {
                "email": "nonprofit@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "generic",
                "country": null,
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 55,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-01-22T13:01:41+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/donatetools.com\/pricing",
                        "extracted_on": "2020-12-15 14:35:50",
                        "last_seen_on": "2021-01-22 13:01:41",
                        "still_on_page": true,
                        "website_url": "donatetools.com"
                    },
                   
                ]
            },
            ...
            ...
            ...
        ]
    },
    "meta": {
        "total": 1514,
        "pageSize": 10,
        "current": 0,
        "total_pages": 152
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
