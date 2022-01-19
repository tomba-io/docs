# Domain status

Returns domain status if is webmail or disposable.

It's free and doesn't require authentication.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/domain-status?domain=gmail.com' \
  --header 'content-type: application/json' \
```

```php
use Tomba\Client;
use Tomba\Services\Status;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$status = new Status($client);

$result = $status->domainStatus('gmail.com');

```

```python
from tomba.client import Client
from tomba.services.status import Status

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

status = Status(client)

result = status.domain_status('gmail.com')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let status = new tomba.Status(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = status.domainStatus('gmail.com');

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

status = Tomba::Status.new(client);

response = status.domain_status(domain: 'gmail.com');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- status(client, domain="gmail.com")
data

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Status status = Status(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = status.domainStatus(
    domain: 'gmail.com',
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

`GET /domain-status/?domain=:domain`

### The parameters are defined as follows

| Parameter | Default  | Description                                                              |
| --------- | -------- | ------------------------------------------------------------------------ |
| `domain`  | Required | Domain name from which you want to check. For example, "gmail.com".      |
| `email`   | Required | Email address from which you want to check. For example, "me@gmail.com". |

<aside class="notice">
We crawl the disposable daily to keep safe from fake uses, if the invalid domain we will set disposable `true` .
</aside>

## Response  Objects details

> Full Response

```json
{
  "domain": "gmail.com",
  "webmail": true,
  "disposable": false
}
```

| Attribute    | Type | Description                 |
| ------------ | ---- | --------------------------- |
| `webmail`    | int  | is webmail email service    |
| `disposable` | int  | is disposable email service |
