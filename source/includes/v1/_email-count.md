# Email Count

Returns total email addresses we have for one domain.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/email-count?domain=google.com' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Count;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$count = new Count($client);

$result = $count->emailCount('tomba.io');

```

```python
from tomba.client import Client
from tomba.services.count import Count

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

count = Count(client)

result = count.email_count('tomba.io')
```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let count = new tomba.Count(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = count.emailCount('tomba.io');

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

count = Tomba::Count.new(client);

response = count.email_count(domain: 'tomba.io');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- count(client, domain="tomba.io")
data

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Count count = Count(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = count.emailCount(
    domain: 'tomba.io',
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

`GET /email-count/?domain=:domain`

### The parameters are defined as follows

| Parameter | Default  | Description                                                                             |
| --------- | -------- | --------------------------------------------------------------------------------------- |
| `domain`  | Required | Domain name from which you want to find the email addresses. For example, "stripe.com". |

## Response Objects details

| Attribute                   | Type | Description                            |
| --------------------------- | ---- | -------------------------------------- |
| `total`                     | int  | Total email                            |
| `personal_emails`           | int  | Total `personal` email                 |
| `generic_emails`            | int  | Total `generic` email                  |
| `department` > `_key_name_` | int  | Total email on department `_key_name_` |
| `seniority` > `_key_name_`  | int  | Total email on seniority `_key_name_`  |
> Full Response

```json
{
  "data": {
    "total": 129283,
    "personal_emails": 129283,
    "generic_emails": 295,
    "department": {
      "engineering": 871,
      "finance": 692,
      "hr": 505,
      "it": 1040,
      "marketing": 4996,
      "operations": 2369,
      "management": 4208,
      "sales": 1455,
      "legal": 208,
      "support": 1414,
      "communication": 226
    },
    "seniority": {
      "junior": 3265,
      "senior": 20948,
      "executive": 4712
    }
  }
}
```
