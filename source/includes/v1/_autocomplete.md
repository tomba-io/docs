# Autocomplete

Company Autocomplete is an API that lets you auto-complete company names and retreive logo and domain information.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/domains-suggestion?query=googl' \
  --header 'Content-Type: application/json' \
```

### HTTP Request

`GET /domains-suggestion?query=:query`

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
      "website_url": "google.com",
      "name": "Google",
      "email_count": 336,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=google.com"
    },
    {
      "website_url": "txt.voice.google.com",
      "name": "Txt",
      "email_count": 2,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=txt.voice.google.com"
    },
    {
      "website_url": "googlegroups.com",
      "name": "Googlegroups",
      "email_count": 5,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=googlegroups.com"
    },
    {
      "website_url": "ooglesngoogles.com",
      "name": "Ooglesngoogles",
      "email_count": 1,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=ooglesngoogles.com"
    },
    {
      "website_url": "googlemail.con",
      "name": "Googlemail",
      "email_count": 2,
      "logo": "https:\/\/www.google.com\/s2\/favicons?sz=24&domain=googlemail.con"
    }
  ],
  "meta": {
    "limit": null,
    "query": "googl"
  }
}
```
