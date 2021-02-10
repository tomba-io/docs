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

| Attribute                   | Type | Description                            |
| --------------------------- | ---- | -------------------------------------- |
| `total`                     | int  | Total email                            |
| `personal_emails`           | int  | Total `personal` email                 |
| `generic_emails`            | int  | Total `generic` email                  |
| `department` > `_key_name_` | int  | Total email on department `_key_name_` |
| `seniority` > `_key_name_`  | int  | Total email on seniority `_key_name_`  |
> Full Response

```json
{
  "data": {
    "total": 129283,
    "personal_emails": 129283,
    "generic_emails": 295,
    "department": {
      "engineering": 871,
      "finance": 692,
      "hr": 505,
      "it": 1040,
      "marketing": 4996,
      "operations": 2369,
      "management": 4208,
      "sales": 1455,
      "legal": 208,
      "support": 1414,
      "communication": 226
    },
    "seniority": {
      "junior": 3265,
      "senior": 20948,
      "executive": 4712
    }
  }
}
```
