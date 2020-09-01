# Companies

## List all your Companies

Returns a list of Companies.

```shell

```

### HTTP Request

`GET /companies/`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": {
    "companies": [
      {
        "id": 1,
        "website": "google.fr",
        "created_at": "2020-06-03 14:53:10",
        "companies_list": {
          "list_id": 22,
          "name": "Nya Dicki"
        }
      }
    ],
    "meta": {
      "total": 1,
      "per_page": 20,
      "current_page": 1,
      "total_pages": 1
    }
  }
}
```

| Attribute                    | Type   | Description       |
| ---------------------------- | ------ | ----------------- |
| `companies`                  | array  | List of companies |
| `id`                         | hash   | Internal ID       |
| `website`                    | string |                   |
| `created_at`                 | string |                   |
| `companies_list` > `list_id` | int    |                   |
| `companies_list` > `name`    | string |                   |

## Get a company

Returns a company.

```shell

```

### HTTP Request

`GET /companies/:id`

### The parameters are defined as follows

| Parameter | Default  | Description     |
| --------- | -------- | --------------- |
| id        | Required | The company ID. |

### Response Objects details

> Full Response

```json
{
  "data": {
    "companies": [
      {
        "id": 1,
        "website": "google.fr",
        "created_at": "2020-06-03 14:53:10",
        "companies_list": {
          "list_id": 22,
          "name": "Nya Dicki"
        }
      }
    ]
  }
}
```

## Create a company

Returns a list of Companies.

```shell

```

### HTTP Request

`POST /companies/`

### The parameters are defined as follows

| Parameter | Default  | Description     |
| --------- | -------- | --------------- |
| id        | Required | The company ID. |

### Response Objects details

> Full Response

```json

```

## Update a company

Returns a list of Companies.

```shell

```

### HTTP Request

`PUT /companies/:id`

### The parameters are defined as follows

| Parameter | Default  | Description     |
| --------- | -------- | --------------- |
| id        | Required | The company ID. |

### Response Objects details

> Full Response

```json

```

## Delete a company

Returns a list of Companies.

```shell

```

### HTTP Request

`DELETE /companies/:id`

### The parameters are defined as follows

| Parameter | Default  | Description     |
| --------- | -------- | --------------- |
| id        | Required | The company ID. |

### Response Objects details

> Full Response

```json

```
