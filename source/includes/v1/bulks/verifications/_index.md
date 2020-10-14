# Bulk Email Verifier

## List all your bulks email verifier

Returns a list of bulks email verifier.

```shell

```

### HTTP Request

`GET /bulk-verifications?secret={YOUR_SECRET}`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Get a bulk email verifier

Returns a Bulk email verifier.

```shell

```

### HTTP Request

`GET /bulk-verifications/:id?secret={YOUR_SECRET}`

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

## Create a bulk email verifier

```shell

```

### HTTP Request

`POST /bulk-verifications?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter | Default  | Description      |
| --------- | -------- | ---------------- |
| `name`    | Required | The bulk name .  |
| `list`    | Required | The email list . |


### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Delete a bulk email verifier

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

`DELETE /bulk-verifications/:id?secret={YOUR_SECRET}`

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
