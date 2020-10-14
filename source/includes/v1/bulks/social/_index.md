# Bulk Social URL

## List all your bulks Social URL

Returns a list of bulks Social URL.

```shell

```

### HTTP Request

`GET /bulk-social?secret={YOUR_SECRET}`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Get a bulk Social URL

Returns a bulk Social URL.

```shell

```

### HTTP Request

`GET /bulk-social/:id?secret={YOUR_SECRET}`

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

## Create a bulk Social URL

```shell

```

### HTTP Request

`POST /bulk-social?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter | Default  | Description           |
| --------- | -------- | --------------------- |
| `name`    | Required | The bulk name .       |
| `list`    | Required | The Social URL list . |

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Delete a bulk Social URL

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

`DELETE /bulk-social/:id?secret={YOUR_SECRET}`

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
