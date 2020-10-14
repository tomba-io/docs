# Companies Lists

## List all your Companies lists

Returns a list of Companies lists.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/companies_list/?format=json&direction=&sortby=' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542'
```

### HTTP Request

`GET /companies_list/`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": [
    {
      "list_id": 11,
      "name": "Isai Predovic",
      "created_at": "2020-08-03 19:41:23",
      "updated_at": "0000-00-00 00:00:00"
    },
    {
      "list_id": 8,
      "name": "Filomena Murazik",
      "created_at": "2020-08-03 19:41:22",
      "updated_at": "0000-00-00 00:00:00"
    },
    ...
    ...
    ...
  ]
}
```

| Attribute    | Type   | Description |
| ------------ | ------ | ----------- |
| `list_id`    | int    |             |
| `name`       | string |             |
| `created_at` | string |             |
| `updated_at` | string |             |

## Get a company list

Returns a company list.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/companies_list/8?format=json&page=&limit=&sortby=' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542'
```

### HTTP Request

`GET /companies_list/:id`

### The parameters are defined as follows

### Response Objects details

> Full Response

```json
{
  "data": [
    {
      "list_id": 8,
      "name": "alert('hello')",
      "created_at": "2020-08-03 19:51:08",
      "updated_at": "2020-08-03 20:51:08"
    }
  ]
}
```

| Attribute    | Type   | Description |
| ------------ | ------ | ----------- |
| `list_id`    | int    |             |
| `name`       | string |             |
| `created_at` | string |             |
| `updated_at` | string |             |


## Create a company list

## Update a company list

## Delete a company list
