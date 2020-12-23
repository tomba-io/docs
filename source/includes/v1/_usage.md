# Usage

Returns a your monthly requests

```shell
curl --request GET \
  --url http://api.hunting.io/v1/usage \
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

### HTTP Request

`GET /usage/`

### Response Objects details

| Attribute                | Type   | Description |
| ------------------------ | ------ | ----------- |
| `data` ->`usage`         | int |             |
| `data` ->`created_at`    | int |             |
| `data` ->`domain`        | int |             |
| `data` ->`finder`        | int |             |
| `data` ->`verifier`      | int |             |
| `data` ->`technologies`  | int |             |
| `data` ->`ip`            | int |             |
| `data` ->`risk`          | int |             |
| `data` ->`website`       | int |             |
| `data` ->`bulk`          | int |             |
| `data` ->`extension`     | int |             |
| `data` ->`api`           | int |             |
| `data` ->`mobile`        | int |             |
| `data` ->`desktop`       | int |             |
| `data` ->`sheets`        | int |             |
| `total` ->`usage`        | int |             |
| `total` ->`created_at`   | int |             |
| `total` ->`domain`       | int |             |
| `total` ->`finder`       | int |             |
| `total` ->`verifier`     | int |             |
| `total` ->`technologies` | int |             |
| `total` ->`ip`           | int |             |
| `total` ->`risk`         | int |             |
| `total` ->`website`      | int |             |
| `total` ->`bulk`         | int |             |
| `total` ->`extension`    | int |             |
| `total` ->`api`          | int |             |
| `total` ->`mobile`       | int |             |
| `total` ->`desktop`      | int |             |
| `total` ->`sheets`       | int |             |

> Full Response

```json
{
  "data": [
    {
      "usage": 155,
      "created_at": "2020-08-01",
      "domain": 0,
      "finder": 3,
      "verifier": 9,
      "technologies": 0,
      "ip": 0,
      "risk": 0,
      "website": 1,
      "bulk": 0,
      "extension": 0,
      "api": 0,
      "mobile": 0,
      "desktop": 0,
      "sheets": 12
    },
    {
      "usage": 300,
      "created_at": "2020-08-02",
      "domain": 0,
      "finder": 3,
      "verifier": 9,
      "technologies": 0,
      "ip": 0,
      "risk": 0,
      "website": 1,
      "bulk": 0,
      "extension": 0,
      "api": 0,
      "mobile": 0,
      "desktop": 0,
      "sheets": 12
    },
   ...
   ...
   ...
   ...
  ],
  "total": {
    "usage": 6673,
    "domain": 80,
    "finder": 45,
    "verifier": 121,
    "technologies": 360,
    "ip": 360,
    "risk": 168,
    "website": 108,
    "bulk": 0,
    "extension": 0,
    "api": 0,
    "mobile": 0,
    "desktop": 0,
    "sheets": 96
  }
}
```
