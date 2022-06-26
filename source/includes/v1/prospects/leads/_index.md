# Leads

## List all your leads

Returns a list of leads.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/leads/' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx'
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

| Parameter   | Default  | Description                                                                |
| ----------- | -------- | -------------------------------------------------------------------------- |
| `page`      | optional | Specifies the number of leads to skip. The default is 1.                   |
| `list`      | optional | lead list ID default is null                                               |
| `limit`     | optional | Specifies the max number of email addresses to return. The default is 10.  |
| `sortby`    | optional | Filter lead by `email`,`first_name`,`last_name`,`country`,`website_url`... |
| `direction` | optional | Filter lead by `desc`,`asc`                                                |

### Response Objects details

| Attribute      | Type   | Description                                                                                                      |
| -------------- | ------ | ---------------------------------------------------------------------------------------------------------------- |
| `id`           | int    | Lead ID                                                                                                          |
| `email`        | string | The email address                                                                                                |
| `first_name`   | string | First name of lead                                                                                               |
| `last_name`    | string | Last name of lead                                                                                                |
| `country`      | string | Two letter country code based on location                                                                        |
| `website_url`  | string | Company domain                                                                                                   |
| `position`     | string | The job title of lead                                                                                            |
| `twitter`      | string | Twitter handle for the lead                                                                                      |
| `linkedin`     | string | LinkedIn URL for the lead                                                                                        |
| `phone_number` | string | The phone number of lead                                                                                         |
| `company`      | string | The company of lead                                                                                              |
| `lead_source`  | string | The lead source default is `null` or one of the following values: `domain`, `finder`, `verify`, `browser`.       |
| `sync_status`  | string | The lead synchronization status default is `null` or one of the following values: `success`, `pending`, `error`. |
| `sync`         | object | sync CRM integrations status                                                                                     |
| `leads_list`   | object | List info                                                                                                        |
| `attributes`   | object | attributes value                                                                                                 |

> Full Response

```json
{
  "data": {
    "leads": [
      {
        "id": 84,
        "user_id": 1,
        "email": "xxx@mozilla.com",
        "first_name": "ed",
        "last_name": "lim",
        "country": "US",
        "website_url": "mozilla.com",
        "position": "senior system administrator",
        "twitter": null,
        "linkedin": "https://www.linkedin.com/in/edwardlim",
        "phone_number": null,
        "company": "Mozilla Toronto",
        "notes": "Notes",
        "score": 95,
        "lead_source": "domain",
        "sync_status": null,
        "sync": {
          "sync_airtable": null,
          "sync_hubspot": null,
          "sync_mailchimp": null,
          "sync_pipedrive": null
        },
        "leads_list": {
          "list_id": 10,
          "name": "test2"
        },
        "attributes": [],
        "created_at": "2021-02-02T23:04:43+01:00",
        "updated_at": "2021-02-09T23:57:41+01:00"
      },
      {
        "id": 83,
        "user_id": 1,
        "email": "xxxx@mozilla.com",
        "first_name": "nick",
        "last_name": "nguyen",
        "country": "US",
        "website_url": "mozilla.com",
        "position": "vp firefox product",
        "twitter": null,
        "linkedin": "https://www.linkedin.com/in/osunick",
        "phone_number": null,
        "company": "Mozilla Toronto",
        "notes": null,
        "score": 95,
        "lead_source": "domain",
        "sync_status": null,
        "sync": {
          "sync_airtable": null,
          "sync_hubspot": null,
          "sync_mailchimp": null,
          "sync_pipedrive": null
        },
        "leads_list": {
          "list_id": 10,
          "name": "test2"
        },
        "attributes": [],
        "created_at": "2021-02-02T23:04:43+01:00",
        "updated_at": "2021-02-09T23:57:41+01:00"
      }
    ],
    "meta": {
      "total": 2,
      "pageSize": 50,
      "current": 1,
      "total_pages": 1
    }
  }
}
```

## Get a lead

Returns a lead.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/leads/2' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx' \
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

| Parameter | Default  | Description |
| --------- | -------- | ----------- |
| `id`      | Required | lead ID .   |

### Response Objects details

| Attribute      | Type   | Description                                                                                                      |
| -------------- | ------ | ---------------------------------------------------------------------------------------------------------------- |
| `id`           | int    | Lead ID                                                                                                          |
| `email`        | string | The email address                                                                                                |
| `first_name`   | string | First name of lead                                                                                               |
| `last_name`    | string | Last name of lead                                                                                                |
| `country`      | string | Two letter country code based on location                                                                        |
| `website_url`  | string | Company domain                                                                                                   |
| `position`     | string | The job title of lead                                                                                            |
| `twitter`      | string | Twitter handle for the lead                                                                                      |
| `linkedin`     | string | LinkedIn URL for the lead                                                                                        |
| `phone_number` | string | The phone number of lead                                                                                         |
| `company`      | string | The company of lead                                                                                              |
| `lead_source`  | string | The lead source default is `null` or one of the following values: `domain`, `finder`, `verify`, `browser`.       |
| `sync_status`  | string | The lead synchronization status default is `null` or one of the following values: `success`, `pending`, `error`. |
| `sync`         | object | sync CRM integrations status                                                                                     |
| `leads_list`   | object | List info                                                                                                        |
| `attributes`   | object | attributes value                                                                                                 |

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

Create a new lead . If the email already exists, fails with `422` status code.

```shell
curl --request POST \
  --url 'https://api.tomba.io/v1/leads' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx' \
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

| Parameter      | Default  | Description                               |
| -------------- | -------- | ----------------------------------------- |
| `email`        | Required | The email address                         |
| `list`         | optional | List ID                                   |
| `first_name`   | optional | First name of lead                        |
| `last_name`    | optional | Last name of lead                         |
| `country`      | optional | Two letter country code based on location |
| `website_url`  | optional | Company domain                            |
| `position`     | optional | The job title of lead                     |
| `twitter`      | optional | Twitter handle for the lead               |
| `linkedin`     | optional | LinkedIn URL for the lead                 |
| `phone_number` | optional | The phone number of lead                  |
| `company`      | optional | The company of lead                       |
| `attributes`   | optional | attributes value                          |

### Response Objects details

| Attribute      | Type | Description |
| -------------- | ---- | ----------- |
| `data` -> `id` | int  | Lead ID     |

> Full Response

```json
{
  "data": {
    "id": 117
  }
}
```

## Update a lead

Update the fields of a lead using `id`.

```shell
curl --request PUT \
  --url 'https://api.tomba.io/v1/leads/278' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx' \
  --data '{
	"email": "mohamed@xasdasd.io",
	"first_name": "Mohamed",
	"last_name": "Mohamed",
	"country": null,
	"website_url": "google.com",
	"position": "CEO",
	"twitter": "moskov",
	"linkedin_url": "dmoskov",
	"phone_number": "",
	"company": "Asana",
	"attributes" :{
		"updatesdsad" : "mo",
		"wee" : "mo",
		"s": "6"

	}
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

`PUT /leads/:id`

### The parameters are defined as follows

| Parameter      | Default  | Description                               |
| -------------- | -------- | ----------------------------------------- |
| `id`           | Required | list ID .                                 |
| `email`        | optional | The email address                         |
| `list`         | optional | List ID                                   |
| `first_name`   | optional | First name of lead                        |
| `last_name`    | optional | Last name of lead                         |
| `country`      | optional | Two letter country code based on location |
| `website_url`  | optional | Company domain                            |
| `position`     | optional | The job title of lead                     |
| `twitter`      | optional | Twitter handle for the lead               |
| `linkedin`     | optional | LinkedIn URL for the lead                 |
| `phone_number` | optional | The phone number of lead                  |
| `company`      | optional | The company of lead                       |
| `attributes`   | optional | attributes value                          |

### Response Objects details

| Attribute | Type   | Description       |
| --------- | ------ | ----------------- |
| `status`  | bool   | `true` if updated |
| `message` | string | note message      |

> Full Response

```json
{
  "status": true,
  "message": "The lead has been updated successfully."
}
```

## Delete a lead

Delete a specific lead by passing `id`.

```shell
curl --request DELETE \
  --url 'https://api.tomba.io/v1/leads/275' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx'
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

`DELETE //v1/leads/:id`

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
  "message": "The lead has been delete successfully."
}
```
