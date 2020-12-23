# keys

## List all your keys

Returns a list of your keys.

<aside class="notice">
The Free plane can create only one key.
</aside>

```shell
curl --request GET \
  --url http://api.hunting.io/v1/keys \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx'

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

`GET /keys/`

### Response Objects details

| Attribute                | Type   | Description                           |
| ------------------------ | ------ | ------------------------------------- |
| `keys` ->`id`            | string | the key ID                            |
| `keys` ->`key`           | string | your hash key always start with `ta_` |
| `keys` ->`ip_addresses`  | string | IP address                            |
| `keys` ->`creation_date` | string | the date of creation of this key      |

> Full Response

```json
{
  "data": {
    "keys": [
      {
        "id": 373,
        "key": "ta_6529b65481a353523c7c435ed62af1421c002",
        "ip_addresses": "1.0.0.0",
        "creation_date": "2020-10-05 15:34:00"
      },
      {
        "id": 372,
        "key": "ta_722xxxxxxxxxxxxx",
        "ip_addresses": "1.0.0.0",
        "creation_date": "2020-10-05 15:33:58"
      },
      {
        "id": 371,
        "key": "ta_5d02d28bbc5955aa5dbc8b01185278bd63b65",
        "ip_addresses": "1.0.0.0",
        "creation_date": "2020-10-05 15:33:56"
      },
      ...
      ...
      ...
      ...
    ]
  }
}
```

## Get a key

Returns a key.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/keys/241' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx'

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

`GET /keys/:id`

### The parameters are defined as follows

| Parameter | Default  | Description |
| --------- | -------- | ----------- |
| id        | Required | Key ID.     |

### Response Objects details

| Attribute                | Type   | Description                      |
| ------------------------ | ------ | -------------------------------- |
| `keys` ->`id`            | string | the key ID                       |
| `keys` ->`key`           | string | your hash key                    |
| `keys` ->`ip_addresses`  | string | IP address                       |
| `keys` ->`creation_date` | string | the date of creation of this key |

> Full Response

```json
{
  "data": {
    "keys": [
      {
        "id": 241,
        "key": "ta_xxxxxxxxxxxxxxxxx",
        "ip_addresses": "1.0.0.1",
        "creation_date": "2020-08-17 17:58:56"
      }
    ]
  }
}
```

## Create a key

```shell
curl --request POST \
  --url 'http://api.hunting.io/v1/keys?secret=df3908be-eb1e-4289-b842-8eff404318dc' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx'

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

`POST /keys`

### Response Objects details

| Attribute | Type   | Description   |
| --------- | ------ | ------------- |
| `id`      | string | the key ID    |
| `key`     | string | your hash key |

> Full Response

```json
{
  "data": {
    "id": 399,
    "key": "ta_5fac2f2628532a6500833dc539971197ec583c59"
  }
}
```

## Rest a key

```shell
curl --request PUT \
  --url 'http://api.hunting.io/v1/keys/2' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx'

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

`PUT /keys/:id`

### The parameters are defined as follows

| Parameter | Default  | Description |
| --------- | -------- | ----------- |
| id        | Required | Key ID.     |

### Response Objects details

| Attribute | Type   |
| --------- | ------ |
| `status`  | bool   |
| `message` | string |

> Full Response

```json
{
  "status": true,
  "message": "The keys has been Rest."
}
```

## Delete a key

```shell
curl --request DELETE \
  --url 'http://api.hunting.io/v1/keys/259' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx'
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

`DELETE /keys/:id`

### The parameters are defined as follows

| Parameter | Default  | Description |
| --------- | -------- | ----------- |
| id        | Required | Key ID.     |

### Response Objects details

| Attribute | Type   |
| --------- | ------ |
| `status`  | bool   |
| `message` | string |

> Full Response

```json
{
  "status": true,
  "message": "The keys has been delete successfully."
}
```
