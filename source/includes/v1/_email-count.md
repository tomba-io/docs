# Email Count

Returns total email addresses we have for one domain.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/email-count?domain=rbr3.com' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: be548b797bfcc3950be4ec9bdba18c91db203ef6'
```

## HTTP Request

`GET /email-count/?domain=:domain`

### The parameters are defined as follows

| Parameter | Default  | Description                                                                             |
| --------- | -------- | --------------------------------------------------------------------------------------- |
| `domain`  | Required | Domain name from which you want to find the email addresses. For example, "stripe.com". |


## Response  Objects details

> Full Response

```json
{
  "data": {
    "total": 5,
    "personal_emails": 1,
    "generic_emails": 4,
    "department": {
      "design": 0,
      "engineering": 0,
      "finance": 0,
      "hr": 0,
      "it": 2,
      "marketing": 0,
      "operations": 0,
      "management": 0,
      "executive": 0,
      "sales": 0,
      "legal": 0,
      "support": 0,
      "communication": 0
    },
    "seniority": {
      "junior": 1,
      "senior": 2,
      "executive": 1
    }
  }
}
```

| Attribute                      | Type | Description            |
| ------------------------------ | ---- | ---------------------- |
| `total`                        | int  | Total email            |
| `personal_emails`              | int  | Total `personal` email |
| `generic_emails`               | int  | Total `generic` email  |
| `department` > `design`        | int  |                        |
| `department` > `engineering`   | int  |                        |
| `department` > `finance`       | int  |                        |
| `department` > `hr`            | int  |                        |
| `department` > `it`            | int  |                        |
| `department` > `marketing`     | int  |                        |
| `department` > `operations`    | int  |                        |
| `department` > `management`    | int  |                        |
| `department` > `executive`     | int  |                        |
| `department` > `sales`         | int  |                        |
| `department` > `legal`         | int  |                        |
| `department` > `support`       | int  |                        |
| `department` > `communication` | int  |                        |
| `seniority` > `junior`         | int  |                        |
| `seniority` > `senior`         | int  |                        |
| `seniority` > `executive`      | int  |                        |
