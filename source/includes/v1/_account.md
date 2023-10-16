# Account Information

Returns information about the current account.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/me' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Account;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$account = new Account($client);

$result = $account->getAccount();

```

```python
from tomba.client import Client
from tomba.services.account import Account

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

account = Account(client)

result = account.get_account()

```

```javascript
const tomba = require("tomba");

// Init Tomba
let client = new tomba.Client();

let account = new tomba.Account(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
let result = account.getAccount();

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

account = Tomba::Account.new(client);

response = account.get_account();

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- account(client)
data
```

```dart
import 'package:tomba/tomba.dart';

void main() {
  // Init SDK
  Client client = Client();
  Account account = Account(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = account.getAccount();

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

`GET /me`

### The parameters are defined as follows

| Parameter | Default  | Description       |
| --------- | -------- | ----------------- |
| `key`     | Required | Your API `key`    |
| `secret`  | Required | Your API `secret` |

## Response Objects details

> Full Response

```json
{
  "data": {
    "user_id": 283,
    "secret_token": "ts_d611fc23-504c-4c13-8943-a48d98db38bf",
    "role": 2,
    "confirmed": true,
    "blocked": false,
    "first_name": "******",
    "last_name": "****",
    "email": "******@tomba.io",
    "phone": "+3550556254142",
    "image": "https://lh3.googleusercontent.com/a/xxxxxx=s96-c",
    "deleted": false,
    "provider": "google",
    "timezone": "XXX/XXXX",
    "newsletter": false,
    "activity": false,
    "title": null,
    "country": "***",
    "created_at": "2021-03-08T14:39:52+01:00",
    "ip": "105.98.231.150",
    "issued": "2023-10-12T12:34:10+02:00",
    "expired": "2023-11-11T11:34:10+01:00",
    "expired_subscription": "2024-06-23T21:58:07+02:00",
    "pricing": {
      "name": "Enterprise",
      "pricing_id": 5,
      "available_searches": 50000,
      "available_verifications": 100000,
      "available_phones": 5000,
      "available_leads": 50000,
      "available_list": 500,
      "available_attr": 29,
      "available_keys": 50,
      "available_teams": 20,
      "available_b2b": 25,
      "available_sources": 500,
      "available_email_count": 80000,
      "frequency": "monthly",
      "price_monthly": "389",
      "price_yearly": "3501",
      "update_url": null,
      "cancel_url": null
    },
    "teams": {
      "team_id": null,
      "role": null,
      "workspace": null,
      "export": null,
      "bulks": null,
      "limit": {
        "search": null,
        "verifier": null
      },
      "owner": null
    },
    "requests": {
      "domains": {
        "available": 50000,
        "used": 51
      },
      "verifications": {
        "available": 100000,
        "used": 1
      },
      "phones": {
        "available": 5000,
        "used": 0
      },
      "b2b": {
        "available": 25,
        "used": 0
      }
    }
  }
}
```
