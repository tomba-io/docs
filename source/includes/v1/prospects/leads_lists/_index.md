# Leads Lists

## List all your leads lists

Returns a list of leads lists.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/leads_lists/' \
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

`GET /leads_lists`

### Response Objects details

| Attribute                    | Type   | Description                                                    |
| ---------------------------- | ------ | -------------------------------------------------------------- |
| `list_leads` -> `id`         | int    | List ID                                                        |
| `list_leads` -> `name`       | string | Name of the List                                               |
| `list_leads` -> `favorite`   | bool   | is the List favorite `true` or `false`                         |
| `list_leads` -> `type`       | string | The type is `campaigns` by default ,Soon we will add more Type |
| `list_leads` -> `size`       | int    | Total lead on this list                                        |
| `list_leads` -> `created_at` | string | The date of creation                                           |
| `list_leads` -> `updated_at` | string | the date when the `list` was updated                           |

> Full Response

```json
{
  "data": {
    "list_leads": [
      {
        "id": 2,
        "name": "html",
        "favorite": false,
        "type": "campaigns",
        "size": 105,
        "created_at": "2020-12-13T07:59:36+01:00",
        "updated_at": "2020-12-13T07:59:36+01:00"
      },
      {
        "id": 3,
        "name": "tgevrt",
        "favorite": false,
        "type": "campaigns",
        "size": 34,
        "created_at": "2020-12-13T08:01:45+01:00",
        "updated_at": "2020-12-13T08:01:45+01:00"
      },
      {
        "id": 436,
        "name": "ce",
        "favorite": false,
        "type": "campaigns",
        "size": 4,
        "created_at": "2020-12-14T10:36:56+01:00",
        "updated_at": "2020-12-14T10:36:56+01:00"
      },
      {
        "id": 462,
        "name": "we",
        "favorite": false,
        "type": "campaigns",
        "size": 0,
        "created_at": "2020-12-14T10:29:17+01:00",
        "updated_at": "2020-12-14T10:29:17+01:00"
      }
    ]
  }
}
```

## Get a leads list

Returns a leads list.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/leads_lists/1' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx' \
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

| Parameter | Default  | Description    |
| --------- | -------- | -------------- |
| `id`      | Required | attribute ID . |

### Response Objects details

| Attribute                    | Type   | Description                                                    |
| ---------------------------- | ------ | -------------------------------------------------------------- |
| `list_leads` -> `id`         | int    | List ID                                                        |
| `list_leads` -> `name`       | string | Name of the List                                               |
| `list_leads` -> `favorite`   | bool   | is the List favorite `true` or `false`                         |
| `list_leads` -> `type`       | string | The type is `campaigns` by default ,Soon we will add more Type |
| `list_leads` -> `size`       | int    | Total lead on this list                                        |
| `list_leads` -> `created_at` | string | The date of creation                                           |
| `list_leads` -> `updated_at` | string | the date when the `list` was updated                           |

> Full Response

```json
{
  "data": [
    {
      "id": 1,
      "name": "html",
      "favorite": false,
      "type": "campaigns",
      "size": 109,
      "created_at": "2020-12-13T07:59:36+01:00",
      "updated_at": "2020-12-21T12:46:35+01:00"
    }
  ]
}
```

## Create a leads list

Create a new leads list with the `name` request parameter. If the list name already exists, fails with `422` status code.

```shell
curl --request POST \
  --url 'https://api.tomba.io/v1/leads_lists/' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx' \
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

| Parameter | Default  | Description      |
| --------- | -------- | ---------------- |
| `name`    | Required | Name of the list |

### Response Objects details

| Attribute           | Type   | Description |
| ------------------- | ------ | ----------- |
| `data` -> `list_id` | int    | List ID     |
| `data` -> `name`    | string | list name   |

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

Update the fields of a list using `id`.

```shell
curl --request PUT \
  --url 'https://api.tomba.io/v1/leads_lists/17' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx' \
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

| Parameter | Default  | Description           |
| --------- | -------- | --------------------- |
| `id`      | Required | list ID .             |
| `name`    | Required | new name for the list |

### Response Objects details

| Attribute | Type   | Description       |
| --------- | ------ | ----------------- |
| `status`  | bool   | `true` if updated |
| `message` | string | note message      |

> Full Response

```json
{
  "status": true,
  "message": "The leads list info has been updated successfully."
}
```

## Delete a leads list

Delete a specific list by passing `id`.

```shell
curl --request DELETE \
  --url 'https://api.tomba.io/v1/leads_lists/5' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx' \
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

| Parameter | Default  | Description |
| --------- | -------- | ----------- |
| `id`      | Required | list ID .   |

### Response Objects details

| Attribute | Type   | Description       |
| --------- | ------ | ----------------- |
| `status`  | bool   | `true` if deleted |
| `message` | string | note message      |

> Full Response

```json
{
  "status": true,
  "message": "The leads list info has been delete successfully."
}
```
