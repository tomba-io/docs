# Bulk Technologies

## List all your bulks technologiess

Returns a list of bulks technologiess.

```shell

```

### HTTP Request

`GET /bulk-technologies?secret={YOUR_SECRET}`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Get a bulk technologies

Returns a Bulk technologies.

```shell

```

### HTTP Request

`GET /bulk-technologies/:id?secret={YOUR_SECRET}`

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

## Create a bulk technologies

```shell

```

### HTTP Request

`POST /bulk-technologies?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter | Default  | Description        |
| --------- | -------- | ------------------ |
| `name`    | Required | The bulk name .    |
| `list`    | Required | The website list . |

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Delete a bulk technologies

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

`DELETE /bulk-technologies/:id?secret={YOUR_SECRET}`

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
