# Leads

## List all your leads

Returns a list of leads.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/leads/?page=1&limit=40&sortby=&direction=&format=' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_722xxxxxxxxxxxxx' \
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

`GET /leads/`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": {
    "leads": [
      {
        "leads_list": {
          "list_id": 22,
          "name": "Nya Dicki"
        },
        "email": "Shanon_Christiansen@yahoo.com",
        "first_name": "Rocky Kohler",
        "last_name": "Beer",
        "country": "MU",
        "website_url": "asana.com",
        "position": "Investor Creative Consultant",
        "twitter": "moskov",
        "linkedin": "ASD",
        "phone_number": "094-306-9130",
        "company": "Metrics",
        "notes": "ASDDDDDDDDDDDD",
        "lead_source": "0",
        "created_at": "2020-06-03 14:53:10",
        "updated_at": "2020-06-03 14:53:10",
        "id": 116
      },
      ...
      ...
      ...
    ],
    "meta": {
      "total": 89,
      "pageSize": 40,
      "current": 1,
      "total_pages": 3
    }
  }
}
```

## Get a lead

Returns a lead.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/leads/2?secret=c18ae4c7-2d78-4c06-9a32-a94bc27bc940&format=json' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_722xxxxxxxxxxxxx' \
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

`GET /leads/:id`

### The parameters are defined as follows



### Response Objects details

> Full Response

```json
{
  "data": {
    "leads": [
      {
        "leads_list": {
          "list_id": 1,
          "name": "Lazaro Reichert"
        },
        "email": "test@rg.fr",
        "first_name": "Moskovitzs",
        "last_name": "Dustinx",
        "country": null,
        "website_url": "asana.com",
        "position": "CEO",
        "twitter": "moskov",
        "linkedin": "dmoskov",
        "phone_number": "",
        "company": "Asana",
        "notes": null,
        "lead_source": "1",
        "created_at": "2020-06-02 19:16:20",
        "updated_at": "0000-00-00 00:00:00",
        "id": 2
      }
    ]
  }
}
```

## Create a lead

```shell
curl --request POST \
  --url 'http://api.hunting.io/v1/leads?secret=c18ae4c7-2d78-4c06-9a32-a94bc27bc940&format=json' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_722xxxxxxxxxxxxx' \
  --data '{
	"list_id": 22,
	"email": "Grover12@hotmail.com",
	"first_name": "Jefferey Hoppe",
	"last_name": "Romaguera",
	"position": "Customer Data Executive",
	"company": "Branding",
	"score": 95,
	"website_url": "asana.com",
	"phone_number": "506-993-3955",
	"twitter": "moskov",
	"country": "UA",
	"linkedin": "ASD",
	"notes": "ASDDDDDDDDDDDD"
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

`POST /leads`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": {
    "id": 117
  }
}
```

## Update a lead

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

`PUT /leads/:id`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```

## Delete a lead

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

`DELETE /domain-search/:domain`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "1": 1
}
```
