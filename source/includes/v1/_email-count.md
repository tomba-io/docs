# Email Count

Returns total email addresses we have for one domain.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/email-count?domain=rbr3.com' \
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
    "total": 8513,
    "personal_emails": 8313,
    "generic_emails": 200,
    "department": {
      "engineering": 52,
      "finance": 44,
      "hr": 10,
      "it": 2,
      "marketing": 58,
      "operations": 40,
      "management": 0,
      "executive": 0,
      "sales": 0,
      "legal": 0,
      "support": 0,
      "communication": 0,
      "software": 0,
      "security": 0,
      "pr": 0,
      "warehouse": 0,
      "diversity": 0,
      "administrative": 0,
      "facilities": 0,
      "accounting": 0
    },
    "seniority": {
      "junior": 152,
      "senior": 88,
      "executive": 0
    }
  }
}
```

