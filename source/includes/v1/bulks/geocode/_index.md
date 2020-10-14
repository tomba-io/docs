# Bulk IP address

## List all your Bulks IP

Returns a list of Bulks IP.

```shell

```

### HTTP Request

`GET /bulk-ip/:domain?secret={YOUR_SECRET}`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Get a Bulk IP

Returns a Bulk IP.

```shell

```

### HTTP Request

`GET /bulk-ip/:id?secret={YOUR_SECRET}`

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

## Create a Bulk IP

```shell

```

### HTTP Request

`POST /bulk-ip/:id?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter | Default  | Description     |
| --------- | -------- | --------------- |
| `name`    | Required | The bulk name . |
| `list`    | Required | The ip list .   |

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Delete a Bulk IP

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

`DELETE /bulk-ip/:id?secret={YOUR_SECRET}`

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
