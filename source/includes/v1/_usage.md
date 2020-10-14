# Usage

Returns a your monthly requests

```shell
curl --request GET \
  --url http://api.hunting.io/v1/usage \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'
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
| `data` ->`usage`         | string |             |
| `data` ->`created_at`    | string |             |
| `data` ->`domain`        | string |             |
| `data` ->`finder`        | string |             |
| `data` ->`verifier`      | string |             |
| `data` ->`technologies`  | string |             |
| `data` ->`ip`            | string |             |
| `data` ->`risk`          | string |             |
| `data` ->`website`       | string |             |
| `data` ->`bulk`          | string |             |
| `data` ->`extension`     | string |             |
| `data` ->`api`           | string |             |
| `data` ->`mobile`        | string |             |
| `data` ->`desktop`       | string |             |
| `data` ->`sheets`        | string |             |
| `total` ->`usage`        | string |             |
| `total` ->`created_at`   | string |             |
| `total` ->`domain`       | string |             |
| `total` ->`finder`       | string |             |
| `total` ->`verifier`     | string |             |
| `total` ->`technologies` | string |             |
| `total` ->`ip`           | string |             |
| `total` ->`risk`         | string |             |
| `total` ->`website`      | string |             |
| `total` ->`bulk`         | string |             |
| `total` ->`extension`    | string |             |
| `total` ->`api`          | string |             |
| `total` ->`mobile`       | string |             |
| `total` ->`desktop`      | string |             |
| `total` ->`sheets`       | string |             |

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
