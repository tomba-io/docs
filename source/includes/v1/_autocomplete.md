# Autocomplete

Company Autocomplete is an API that lets you auto-complete company names and retreive logo and domain information.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/domains-suggestion?query=rb' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api'
```

### HTTP Request

`GET /domains-suggestion?query=:name`

### The parameters are defined as follows

| Parameter | Default  | Description                     |
| --------- | -------- | ------------------------------- |
| query     | Required | name of the company or website. |


### Response Objects details

| Attribute               | Type   | Description            |
| ----------------------- | ------ | ---------------------- |
| `data` -> `email_count` | int    | Total email on company |
| `data` -> `website_url` | string | Domain website         |
| `data` -> `name`        | string | Domain name of company |
| `data` -> `logo`        | string | URL to logo            |

> Full Response

```json
{
  "data": [
    {
      "email_count": 22,
      "website_url": "rbr3.com",
      "name": "Rebein Brothers Law Firm",
      "logo": "https:\/\/logo.tomba.com\/rbr3.com"
    }
    ...
    ...
    ...
    ...
    ...
    ...
    ...
  ],
  "meta": {
    "limit": null,
    "query": "rb"
  }
}
```
