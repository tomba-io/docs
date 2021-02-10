# Email Count

Returns total email addresses we have for one domain.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/email-count?domain=google.com' \
  --header 'content-type: application/json' \
  --header 'x-tannin-key: ta_722xxxxxxxxxxxxx'
```

## HTTP Request

`GET /email-count/?domain=:domain`

### The parameters are defined as follows

| Parameter | Default  | Description                                                                             |
| --------- | -------- | --------------------------------------------------------------------------------------- |
| `domain`  | Required | Domain name from which you want to find the email addresses. For example, "stripe.com". |

## Response Objects details

| Attribute                   | Type | Description              |
| --------------------------- | ---- | ------------------------ |
| `total`                     | int  | Total email              |
| `personal_emails`           | int  | Total `personal` email   |
| `generic_emails`            | int  | Total `generic` email    |
| `department` > `_key_name_` | int  | Total `_key_name_` email |
> Full Response

```json
{
  "data": {
    "total": 336,
    "personal_emails": 334,
    "generic_emails": 2,
    "department": {
      "design": 0,
      "engineering": 0,
      "finance": 1,
      "hr": 0,
      "it": 0,
      "marketing": 2,
      "operations": 0,
      "management": 0,
      "sales": 2,
      "legal": 0,
      "support": 0,
      "communication": 0
    },
    "seniority": {
      "junior": 0,
      "senior": 8,
      "executive": 0
    }
  }
}
```
