# keys

## List all your keys

Returns a list of your keys.

<aside class="notice">
The Free plane can create only one key.
</aside>

```shell
curl --request GET \
  --url https://api.tomba.io/v1/keys \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'

```

```php
use Tomba\Client;
use Tomba\Services\Keys;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$keys = new Keys($client);

$result = $keys->getKeys();

```

```python
from tomba.client import Client
from tomba.services.keys import Keys

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

keys = Keys(client)

result = keys.get_keys()

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let keys = new tomba.Keys(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = keys.getKeys();

result
  .then((response) => {
    console.log(response);
  })
  .catch((err) => {
    console.log(err);
  });
```

```ruby
require 'tomba'

client = Tomba::Client.new()

client
    .set_key('ta_xxxx') # Your Key
    .set_secret('ts_xxxx') # Your Secret
;

keys = Tomba::Keys.new(client);

response = keys.get_keys();

puts response

```

```java
import io.tomba.api.Tomba;

```

```r

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Keys keys = Keys(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = keys.getKeys();

  result
    .then((response) {
      print(response);
    }).catchError((error) {
      print(error.response);
  });
}

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
        "id": 432,
        "key": "ta_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
        "ip_addresses": "127.0.0.1",
        "creation_date": "2021-01-13T01:00:41+01:00"
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
  --url 'https://api.tomba.io/v1/keys/241' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'

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
        "creation_date": "2021-01-13T00:45:05+01:00"
      }
    ]
  }
}
```

## Create a key

```shell
curl --request POST \
  --url 'https://api.tomba.io/v1/keys' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'

```

```php
use Tomba\Client;
use Tomba\Services\Keys;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$keys = new Keys($client);

$result = $keys->createKey();

```

```python
from tomba.client import Client
from tomba.services.keys import Keys

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

keys = Keys(client)

result = keys.create_key()

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let keys = new tomba.Keys(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = keys.createKey();

result
  .then((response) => {
    console.log(response);
  })
  .catch((err) => {
    console.log(err);
  });
```

```ruby
require 'tomba'

client = Tomba::Client.new()

client
    .set_key('ta_xxxx') # Your Key
    .set_secret('ts_xxxx') # Your Secret
;

keys = Tomba::Keys.new(client);

response = keys.create_key();

puts response
```

```java
import io.tomba.api.Tomba;

```

```r

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Keys keys = Keys(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = keys.createKey();

  result
    .then((response) {
      print(response);
    }).catchError((error) {
      print(error.response);
  });
}

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
    "key": "ta_xxxxxx"
  }
}
```

## Rest a key

```shell
curl --request PUT \
  --url 'https://api.tomba.io/v1/keys/2' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'

```

```php
use Tomba\Client;
use Tomba\Services\Keys;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$keys = new Keys($client);

$result = $keys->resetKey('2');

```

```python
from tomba.client import Client
from tomba.services.keys import Keys

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

keys = Keys(client)

result = keys.reset_key('')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let keys = new tomba.Keys(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = keys.resetKey('');

result
  .then((response) => {
    console.log(response);
  })
  .catch((err) => {
    console.log(err);
  });
```

```ruby
require 'tomba'

client = Tomba::Client.new()

client
    .set_key('ta_xxxx') # Your Key
    .set_secret('ts_xxxx') # Your Secret
;

keys = Tomba::Keys.new(client);

response = keys.reset_key(id: '');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Keys keys = Keys(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = keys.resetKey(
    id: '',
  );

  result
    .then((response) {
      print(response);
    }).catchError((error) {
      print(error.response);
  });
}
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
  --url 'https://api.tomba.io/v1/keys/259' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Keys;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$keys = new Keys($client);

$result = $keys->deleteKey('259');

```

```python
from tomba.client import Client
from tomba.services.keys import Keys

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

keys = Keys(client)

result = keys.delete_key('')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let keys = new tomba.Keys(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = keys.deleteKey('12');

result
  .then((response) => {
    console.log(response);
  })
  .catch((err) => {
    console.log(err);
  });
```

```ruby
require 'tomba'

client = Tomba::Client.new()

client
    .set_key('ta_xxxx') # Your Key
    .set_secret('ts_xxxx') # Your Secret
;

keys = Tomba::Keys.new(client);

response = keys.delete_key(id: '');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Keys keys = Keys(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = keys.deleteKey(
    id: '',
  );

  result
    .then((response) {
      print(response);
    }).catchError((error) {
      print(error.response);
  });
}

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
