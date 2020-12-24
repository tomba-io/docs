# Lead Attributes

## List all your lead attributes

Returns a list of Lead Attributes.

```shell
curl --request GET \
  --url http://api.hunting.io/v1/leads/attributes \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX'
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

`GET /leads/attributes/`

### The parameters are defined as follows

### Response Objects details

| Attribute                       | Type   | Description                                          |
| ------------------------------- | ------ | ---------------------------------------------------- |
| `attributes` -> `id`            | int    | attribute ID                                         |
| `attributes` -> `name`          | string | Name of the custom attribute                         |
| `attributes` -> `identifier`    | string | identifier of attribute read only It can't be edited |
| `attributes` -> `type`          | string | type attributes `string`, `date`, `number` only.     |
| `attributes` -> `date_created`  | string | The date of creation                                 |
| `attributes` -> `date_modified` | string | the date when the `attr` was updated                 |

> Full Response

```json
{
  "data": {
    "attributes": [
      {
        "id": 48,
        "name": "ALLO",
        "identifier": "allo",
        "type": "string",
        "date_created": "2020-12-11T08:18:37+01:00",
        "date_modified": "2020-12-13T08:47:22+01:00"
      },
      {
        "id": 47,
        "name": "ASD ASD",
        "identifier": "asd_asd",
        "type": "date",
        "date_created": "2020-12-11T08:16:22+01:00",
        "date_modified": "2020-12-11T08:16:22+01:00"
      },
      {
        "id": 46,
        "name": "AS ASD",
        "identifier": "as-asd",
        "type": "number",
        "date_created": "2020-12-11T08:15:47+01:00",
        "date_modified": "2020-12-11T08:15:47+01:00"
      },
      {
        "id": 6,
        "name": "s",
        "identifier": "s",
        "type": "number",
        "date_created": "2020-12-09T03:35:41+01:00",
        "date_modified": "2020-12-09T03:35:55+01:00"
      },
      {
        "id": 5,
        "name": "swe",
        "identifier": "swe",
        "type": "date",
        "date_created": "2020-12-09T03:35:15+01:00",
        "date_modified": "2020-12-09T03:35:15+01:00"
      },
      {
        "id": 4,
        "name": "wee",
        "identifier": "wee",
        "type": "string",
        "date_created": "2020-12-09T03:34:24+01:00",
        "date_modified": "2020-12-09T03:34:24+01:00"
      },
      {
        "id": 3,
        "name": "xxx",
        "identifier": "xxx",
        "type": "string",
        "date_created": "2020-12-09T03:03:17+01:00",
        "date_modified": "2020-12-09T03:33:18+01:00"
      },
      {
        "id": 2,
        "name": "updatesdsad",
        "identifier": "updatesdsad",
        "type": "string",
        "date_created": "2020-12-09T03:02:55+01:00",
        "date_modified": "2020-12-12T09:20:19+01:00"
      },
      {
        "id": 1,
        "name": "ssssss",
        "identifier": "ssssss",
        "type": "date",
        "date_created": "2020-12-07T05:37:53+01:00",
        "date_modified": "2020-12-09T03:33:31+01:00"
      }
    ],
    "meta": {
      "total": 9,
      "pageSize": 50,
      "current": 1,
      "total_pages": 1
    }
  }
}
```

## Get a attributes

Returns a Lead Attributes.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/leads/attributes/38?format=json' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_256390b87e59e33eed1353724a2c65214f266'
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

`GET /leads/attributes/:id`

### The parameters are defined as follows

| Parameter | Default  | Description    |
| --------- | -------- | -------------- |
| `id`      | Required | attribute ID . |

### Response Objects details

| Attribute                       | Type   | Description                                          |
| ------------------------------- | ------ | ---------------------------------------------------- |
| `attributes` -> `id`            | int    | attribute ID                                         |
| `attributes` -> `name`          | string | Name of the custom attribute                         |
| `attributes` -> `identifier`    | string | identifier of attribute read only It can't be edited |
| `attributes` -> `type`          | string | type attributes `string`, `date`, `number` only.     |
| `attributes` -> `date_created`  | string | The date of creation                                 |
| `attributes` -> `date_modified` | string | the date when the `attr` was updated                 |

> Full Response

```json
{
  "data": {
    "attributes": [
      {
        "id": 38,
        "name": "salary",
        "type": "number",
        "date_created": "2020-12-07T05:37:53+01:00",
        "date_modified": "2020-12-07T05:37:53+01:00"
      }
    ]
  }
}
```

## Create a Lead Attributes

Create a new Attributes with the `name` and `type` request parameter. If the Attributes name already exists, fails with `422` status code.

```shell
curl --request POST \
  --url 'http://api.hunting.io/v1/leads/attributes?format=json' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_256390b87e59e33eed1353724a2c65214f266' \
  --data '{"name": "Millie","type": "date"}'
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

`POST /leads/attributes`

### The parameters are defined as follows

| Parameter | Default  | Description                                      |
| --------- | -------- | ------------------------------------------------ |
| `name`    | Required | Name of the custom attribute                     |
| `type`    | Required | type attributes `string`, `date`, `number` only. |

### Response Objects details

| Attribute      | Type | Description  |
| -------------- | ---- | ------------ |
| `data` -> `id` | int  | attribute ID |

> Full Response

```json
{
  "data": {
    "id": 51
  }
}
```

## Update a Lead Attributes

Update the fields of a Attributes using `id`.

```shell
curl --request PUT \
  --url 'http://api.hunting.io/v1//leads/attributes/41?format=json' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_256390b87e59e33eed1353724a2c65214f266' \
  --data '{"name": "total ","type": "string"}'
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

`PUT /leads/attributes/:id`

### The parameters are defined as follows

| Parameter | Default  | Description                                      |
| --------- | -------- | ------------------------------------------------ |
| `id`      | Required | attribute ID .                                   |
| `name`    | Required | Name of the custom attribute                     |
| `type`    | Required | type attributes `string`, `date`, `number` only. |

### Response Objects details

| Attribute | Type   | Description       |
| --------- | ------ | ----------------- |
| `status`  | bool   | `true` if updated |
| `message` | string | note message      |

> Full Response

```json
{
  "status": true,
  "message": "The leads lists info has been updated successfully."
}
```

## Delete a Lead Attributes

Delete a specific Attributes by passing `id`.

```shell
curl --request DELETE \
  --url 'http://api.hunting.io/v1//leads/attributes?format=json' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_256390b87e59e33eed1353724a2c65214f266'
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

`DELETE /leads/attributes/:id`

### The parameters are defined as follows

| Parameter | Default  | Description    |
| --------- | -------- | -------------- |
| `id`      | Required | attribute ID . |

### Response Objects details

| Attribute | Type   | Description       |
| --------- | ------ | ----------------- |
| `status`  | bool   | `true` if deleted |
| `message` | string | note message      |

> Full Response

```json
{
  "status": true,
  "message": "The attributes has been delete successfully."
}
```
