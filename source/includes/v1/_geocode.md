# IP address

Returns a IP address information

```shell
curl --request GET \
  --url http://api.hunting.io/v1/ip/2.2.2.2 \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'
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

`GET /ip/:ip`

### The parameters are defined as follows

| Parameter | Default  | Description                                                                                      |
| --------- | -------- | ------------------------------------------------------------------------------------------------ |
| `ip`      | optional | if you pass a single IPv4 or IPv6 IP address, else you will lookup your IP address information . |

## Response  Objects details

> Full Response

```json
{
  "ip": "2.2.2.2",
  "location": {
    "asn": 3215,
    "country": "FR",
    "stateprov": "Île-de-France",
    "city": "Aubervilliers",
    "latitude": "48.9123",
    "longitude": "2.38405",
    "name": "France",
    "continent_name": "Europe",
    "top_level_domain": ".fr",
    "alpha3_code": "FRA",
    "timezones": "UTC−10:00",
    "currencies": "EUR",
    "currencies_name": "Euro",
    "type": "IPV4"
  },
  "connection": {
    "country": "FR",
    "organization": "Orange S.A.",
    "asn": 3215,
    "website": "orange.fr",
    "comany_type": "isp"
  }
}
```

| Attribute                       | Type   | Description |
| ------------------------------- | ------ | ----------- |
| `ip`                            | string |
| `location` > `asn`              | int    |
| `location` > `country`          | string |
| `location` > `stateprov`        | string |
| `location` > `city`             | string |
| `location` > `latitude`         | string |
| `location` > `longitude`        | string |
| `location` > `name`             | string |
| `location` > `continent_name`   | string |
| `location` > `top_level_domain` | string |
| `location` > `alpha3_code`      | string |
| `location` > `timezones`        | string |
| `location` > `currencies`       | string |
| `location` > `currencies_name`  | string |
| `location` > `type`             | string |
| `connection` > `country`        | string |
| `connection` > `organization`   | string |
| `connection` > `asn`            | int    |
| `connection` > `website`        | string |
| `connection` > `comany_type`    | string |
