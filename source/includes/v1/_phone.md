# Phone Finder

Search phone are based on the email
You give one email and it returns phone data

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/phone/******@zapier.com' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

## HTTP Request

`GET /phone/:email`

### The parameters are defined as follows

| Parameter | Default  | Description                              |
| --------- | -------- | ---------------------------------------- |
| `email`   | Required | The email address you want to find phone |

## Response Objects details

> Full Response

```json
{
  "data": {
    "email": "******@zapier.com",
    "valid": true,
    "local_format": "(877) 381-8743",
    "intl_format": "+1 877-381-8743",
    "e164_format": "+18773818743",
    "rfc3966_format": "tel:+1-877-381-8743",
    "country_code": "US",
    "line_type": "TOLL_FREE",
    "carrier": null,
    "timezones": "America/Adak"
  }
}
```

| Attribute        | Type   | Description                           |
| ---------------- | ------ | ------------------------------------- |
| `email`          | string | returns The email address to look up. |
| `valid`          | bool   | returns the status of the phone.      |
| `local_format`   | string | returns the local format              |
| `intl_format`    | string | returns the international format      |
| `e164_format`    | string | returns the e164 format               |
| `rfc3966_format` | string | returns the rfc3966 format            |
| `country_code`   | string | returns the phone country code        |
| `line_type`      | string | returns the phone type line           |
| `carrier`        | string | returns the phone carrier             |
| `timezones`      | string | returns the phone timezones           |
