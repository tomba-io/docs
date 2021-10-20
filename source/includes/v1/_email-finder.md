# Email Finder

This API endpoint generates or retrieves the most likely email address from a domain name, a first name and a last name.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/email-finder/asana.com?first_name=Moskoz&last_name=Dustin' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Finder;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$finder = new Finder($client);

$result = $finder->emailFinder('stripe.com', 'fname', 'lname');.

```

```python
from tomba.client import Client
from tomba.services.finder import Finder

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

finder = Finder(client)

result = finder.email_finder('stripe.com', 'Moskoz', 'Dustin')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let finder = new tomba.Finder(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = finder.emailFinder('stripe.com', 'fname', 'lname');

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

finder = Tomba::Finder.new(client);

response = finder.email_finder(domain: 'stripe.com', first_name: 'Moskoz', last_name: 'Dustin');

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
    "email": "jan.marek@g-in.cz",
    "first_name": "Jan",
    "last_name": "Marek",
    "full_name": "Jan Marek",
    "country": "CZ",
    "position": null,
    "twitter": null,
    "linkedin": "https://www.linkedin.com/in/jan-marek-245b85103",
    "phone_number": null,
    "accept_all": null,
    "website_url": "g-incz",
    "company": "Garp integ.rated",
    "score": 80,
    "verification": {
      "date": null,
      "status": null
    },
    "sources": []
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
| `phone_number` | bool   | true if found                                                                                                              |
| `company`      | string | The company of person (if found)                                                                                           |
| `last_updated` | string | The time at which we update this data                                                                                      |
