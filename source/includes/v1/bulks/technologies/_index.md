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
