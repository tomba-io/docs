# IP address

Returns a IP address information

```shell
curl --request GET \
  --url http://api.hunting.io/v1/ip/2.2.2.2 \
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

| Attribute                      | Type   | Description                                               |
| ------------------------------ | ------ | --------------------------------------------------------- |
| `ip`                           | string | The requested IP address                                  |
| `location` > `asn`             | int    | The AS number                                             |
| `location` > `country`         | string | The ISO 3166-1 alpha-2 country code                       |
| `location` > `stateprov`       | string | The State or province name                                |
| `location` > `city`            | string | The City name                                             |
| `location` > `latitude`        | string | The Decimal latitude                                      |
| `location` > `longitude`       | string | The Decimal longitude                                     |
| `location` > `name`            | string | The Country name                                          |
| `location` > `continent_name`  | string | The 2-letter continent code                               |
| `location` > `alpha3_code`     | string | The ISO 3166-1 alpha-3 country code                       |
| `location` > `timezones`       | string | The UTC                                                   |
| `location` > `currencies`      | string | The code of the given currency.                           |
| `location` > `currencies_name` | string | The name of the given currency.                           |
| `location` > `type`            | string | IP address type `ipv4` or `ipv6`                          |
| `connection` > `country`       | string | The ISO 3166-1 alpha-2 country code                       |
| `connection` > `organization`  | string | The name of the organization associated with the `asn`    |
| `connection` > `asn`           | int    | The AS number                                             |
| `connection` > `website`       | string | The Website of Organization                               |
| `connection` > `comany_type`   | string | The Organization type ,`business`,`hosting`,`isp`,`other` |
