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
