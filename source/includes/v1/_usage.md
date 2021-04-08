# Usage

Returns a your monthly requests

```shell
curl --request GET \
  --url https://api.tomba.io/v1/usage \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'
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

| Attribute             | Type | Description             |
| --------------------- | ---- | ----------------------- |
| `data` ->`usage`      | int  | total usage on date     |
| `data` ->`created_at` | int  | usage date              |
| `data` ->`name`       | int  | total usage on the name |


> Full Response

```json
{
  "data": [
       {
      "usage": 2,
      "created_at": "2021-01-17",
      "domain": 0,
      "finder": 0,
      "verifier": 2,
      "technologies": 0,
      "ip": 0,
      "website": 0,
      "bulk": 0,
      "extension": 0,
      "api": 0,
      "mobile": 0,
      "desktop": 0,
      "sheets": 0
    },
    {
      "usage": 0,
      "created_at": "2021-01-19",
      "domain": 0,
      "finder": 0,
      "verifier": 0,
      "technologies": 0,
      "ip": 0,
      "website": 0,
      "bulk": 0,
      "extension": 0,
      "api": 0,
      "mobile": 0,
      "desktop": 0,
      "sheets": 0
    },
   ...
   ...
   ...
   ...
  ],
  "total": {
    "usage": 227,
    "domain": 0,
    "finder": 158,
    "verifier": 35,
    "socail": 0,
    "technologies": 0,
    "website": 0,
    "bulk": 0,
    "extension": 0,
    "api": 0,
    "mobile": 0,
    "desktop": 0,
    "sheets": 0
  }
}
```
