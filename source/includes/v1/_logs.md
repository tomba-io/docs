# Logs

Returns a your monthly requests logs

```shell
curl --request GET \
  --url http://api.hunting.io/v1/logs \
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

`GET /logs/`

### Response Objects details

| Attribute              | Type   | Description |
| ---------------------- | ------ | ----------- |
| `data` -> `uri`        | string |             |
| `data` -> `user_agent` | string |             |
| `data` -> `cost`       | bool   |             |
| `data` -> `ip_address` | string |             |
| `data` -> `created_at` | string |             |

> Full Response

```json
{
  "data": [
    {
      "uri": "https:\/\/api.tomba\/v1\/email-finder\/asana.com",
      "user_agent": "tomba api",
      "cost": false,
      "ip_address": "127.0.0.1",
      "created_at": "2020-08-16 18:40:35"
    },
    {
      "uri": "https:\/\/api.tomba\/v1\/email-finder\/asana.com",
      "user_agent": "tomba api",
      "cost": true,
      "ip_address": "127.0.0.1",
      "created_at": "2020-08-16 18:40:30"
    },
    ...
    ...
    ...
    ...
    ...
    ...
  ]
}
```
