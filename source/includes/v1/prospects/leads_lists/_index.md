# Leads Lists

## List all your leads lists

Returns a list of leads lists.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/leads_lists/' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542'
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

`GET /leads_lists`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": [
    {
      "list_id": 1,
      "name": "Lazaro Reichert",
      "created_at": "2020-06-02 19:16:20",
      "updated_at": "0000-00-00 00:00:00"
    },
    {
      "list_id": 8,
      "name": "Filomena Murazik",
      "created_at": "2020-06-02 19:16:20",
      "updated_at": "0000-00-00 00:00:00"
    },
    ...
    ...
  ]
}
```

## Get a leads list

Returns a leads list.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/leads_lists/1' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542' \
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

`GET /leads_lists/:id`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": [
    {
      "list_id": 1,
      "name": "Lazaro Reichert",
      "created_at": "2020-06-02 19:16:20",
      "updated_at": "0000-00-00 00:00:00"
    }
  ]
}
```

## Create a leads list

```shell
curl --request POST \
  --url 'http://api.hunting.io/v1/leads_lists/' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542' \
  --data '{
  "name": "Mario Monahan"
  }'
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

`POST /leads_lists`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": {
    "list_id": 22,
    "name": "Nya Dicki"
  }
}
```

## Update a leads list

```shell
curl --request PUT \
  --url 'http://api.hunting.io/v1/leads_lists/17' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542' \
  --data '{
  "name": "update listsssssssssss"
  }'
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

`PUT /leads_lists/:id`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "status": true,
  "message": "The leads list info has been updated successfully."
}
```

## Delete a leads list

```shell
curl --request DELETE \
  --url 'http://api.hunting.io/v1/leads_lists/5' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542' \
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

`DELETE /leads_lists/:id`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "status": true,
  "message": "The leads list info has been delete successfully."
}
```
