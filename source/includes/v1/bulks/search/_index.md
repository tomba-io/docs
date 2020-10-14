# Bulk Domain Search

## List all your bulks domains

Returns a list of bulks domains.

```shell

```

### HTTP Request

`GET /bulk-searches?secret={YOUR_SECRET}`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Get a bulk domain

Returns a Bulk domain.

```shell

```

### HTTP Request

`GET /bulk-searches/:id?secret={YOUR_SECRET}`

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

## Create a bulk domain

```shell

```

### HTTP Request

`POST /bulk-searches?secret={YOUR_SECRET}`

### The parameters are defined as follows

| Parameter       | Default  | Description                               |
| --------------- | -------- | ----------------------------------------- |
| `name`          | Required | The bulk name .                           |
| `list`          | Required | The domains names .                       |
| `maximum_email` | Required | Maximum email addresses per domain .      |
| `email_type`    | Required | The Email addresses type .                |
| `department`    | Required | The Department type .                     |
| `sources`       | Required | The Include the sources in the result   . |

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```


## Delete a bulk domain

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

`DELETE /bulk-searches/:id?secret={YOUR_SECRET}`

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
