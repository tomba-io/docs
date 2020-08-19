# keys

## List all your keys

Returns a list of keys.

```shell
curl --request GET \
  --url http://api.hunting.io/v1/keys \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'

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

`GET /keys/`

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
        "id": "241",
        "key": "bsad548b797bfcc395xxxxxxxxx",
        "ip_addresses": "127.0.0.1",
        "creation_date": "2020-08-17 17:58:56"
      },
      {
        "id": "245",
        "key": "be548b797bfcc395xxxxxxxxx",
        "ip_addresses": "127.0.0.1",
        "creation_date": "2020-08-17 17:59:54"
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
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'

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
        "key": "xxxxxxxxxxxxxxxxx",
        "ip_addresses": "127.0.0.1",
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
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'

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
    "id": 259,
    "key": "522f5429e6ccedfbe08xxxxxxxxxxxxxxx"
  }
}
```

## Rest a key

```shell
curl --request PUT \
  --url 'http://api.hunting.io/v1/keys/2' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'

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

`PUT /keys/:id`

### The parameters are defined as follows

| Parameter | Default  | Description |
| --------- | -------- | ----------- |
| id        | Required | Key ID.     |

### Response Objects details

| Attribute | Type   | Description |
| --------- | ------ | ----------- |
| `status`  | bool   |             |
| `message` | string |             |

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
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'
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

`DELETE /keys/:id`

### The parameters are defined as follows

| Parameter | Default  | Description |
| --------- | -------- | ----------- |
| id        | Required | Key ID.     |

### Response Objects details

| Attribute | Type   | Description |
| --------- | ------ | ----------- |
| `status`  | bool   |             |
| `message` | string |             |

> Full Response

```json
{
  "status": true,
  "message": "The keys has been delete successfully."
}
```
