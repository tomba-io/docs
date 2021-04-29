## Email Sources

Find email address source somewhere on the web  

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/email-sources/b.mohamed@tomba.io' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ts_xxxx'
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

`GET /email-sources/:email`

### The parameters are defined as follows

| Parameter | Default  | Description                                 |
| --------- | -------- | ------------------------------------------- |
| `email`   | Required | The email address you want to find sources. |

## Response  Objects details

> Full Response

```json
{
    "email": "b.mohamed@tomba.io",
    "data": [
        {
            "uri": "https:\/\/github.com\/tomba-io\/generic-emails\/blob\/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9\/src\/lib\/validation\/hash.ts",
            "extracted_on": "2021-02-08T20:09:54+01:00",
            "last_seen_on": "2021-02-08T22:43:40+01:00",
            "still_on_page": true,
            "website_url": "github.com"
        },
        {
            "uri": "https:\/\/github.com\/tomba-io\/generic-emails\/blame\/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9\/src\/lib\/validation\/hash.ts",
            "extracted_on": "2021-02-08T20:09:59+01:00",
            "last_seen_on": "2021-02-08T22:43:40+01:00",
            "still_on_page": true,
            "website_url": "github.com"
        }
    ]
}
```

| Attribute | Type   | Description                                  |
| --------- | ------ | -------------------------------------------- |
| `email`   | string | The email address to look up.                |
| `source`  | array  | The given email address somewhere on the web |
