# Bulk Email Finder

## List all Bulks Emails

Returns a list of Bulks Emails.

```shell

```

### HTTP Request

`GET /bulk-finders?secret={YOUR_SECRET}`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Get a Bulk Email

Returns a Bulk Email.

```shell

```

### HTTP Request

`GET /bulk-finders/:id?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter | Default  | Description  |
| --------- | -------- | ------------ |
| id        | Required | The bulk ID. |

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Create a Bulk Email

```shell

```

### HTTP Request

`POST /bulk-finders/:id?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter | Default  | Description                                      |
| --------- | -------- | ------------------------------------------------ |
| `name`    | Required | The bulk name .                                  |
| `list`    | Required | The list : first name and last name and domain . |
| `sources` | Required | The Include the sources in the result   .        |

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Delete a Bulk Email

```shell

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

`DELETE /bulk-finders/:id?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter | Default  | Description  |
| --------- | -------- | ------------ |
| id        | Required | The bulk ID. |

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```
