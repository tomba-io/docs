# Domain status

Returns domain status if is webmail or disposable.

It's free and doesn't require authentication.

```shell
curl --request GET \
  --url 'http://api.hunting.io/v1/domain-status?domain=gmail.com' \
  --header 'content-type: application/json' \
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
  "domain": "gmail.com",
  "webmail": true,
  "disposable": false
}
```

| Attribute    | Type | Description                 |
| ------------ | ---- | --------------------------- |
| `webmail`    | int  | is webmail email service    |
| `disposable` | int  | is disposable email service |
