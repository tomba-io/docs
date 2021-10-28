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
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let account = new tomba.Account(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

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

## Response  Objects details

> Full Response

```json
{
    "data": {
        "available": 5000,
        "user_id": 1,
        "secret_token": "ts_xxx",
        "role": 2,
        "confirmed": true,
        "blocked": false,
        "first_name": "xxx",
        "last_name": "xxxx",
        "email": "xxx@tomba.io",
        "phone": "+xxxxxxx",
        "image": "https:\/\/www.gravatar.com\/avatar\/xxxxxxxxx?s=128&d=https:\/\/ui-avatars.com\/api\/M+B\/128\/001529\/fff?ssl=1",
        "deleted": false,
        "timezone": "xx\/xx",
        "newletter": false,
        "activity": false,
        "title": "",
        "country": "AU",
        "created_at": "2020-02-18T15:52:10+01:00",
        "ip": "1.0.0.0",
        "payment_status": true,
        "issued": "2020-12-22T15:52:10+01:00",
        "expired": "2021-10-24T00:00:00+01:00",
        "pricing": {
            "name": "Growth",
            "pricing_id": 3,
            "available_searches": 2500,
            "available_verifications": 2500,
            "available_phones": 500,
            "available_leads": 10000,
            "available_list": 150,
            "available_attr": 29,
            "available_keys": 10,
            "available_teams": 5,
            "available_email_count": 10000,
            "frequency": "monthly"
        },
        "time": {
            "date": "2021-01-31 21:23:00.997965",
            "timezone_type": 3,
            "timezone": "xx\/xxxx"
        },
        "used": 1349,
        "requests": {
            "domains": {
                "available": 2500,
                "used": 12
            },
            "verifications": {
                "available": 2500,
                "used": 49
            },
            "phones": {
                "available": 500,
                "used": 17
            }
        }
    }
}
```
