# Risk API

You can ping the Risk REST API with an email & IP address to calculate a risk score. We’ll also return some information about the parameters, for example indicating if the email is disposable or the IP belongs to a proxy.

For testing, you can provide the loopback IP address `127.0.0.1`. That’ll switch off some of the things we do that don’t make sense in a testing environment like velocity checks.

```shell
curl --request POST \
  --url 'http://api.hunting.io/v1/risk?secret=df3908be-eb1e-4289-b842-8eff404318dc' \
  --header 'content-type: application/json' \
  --header 'user-agent: tomba api' \
  --header 'x-tannin-key: ta_722ec46dc745c2224fb3bd6edbd44e7800542' \
  --data '{
    "email" : "EMAIL",
    "ip" : "IP address",
    "country_code" : "country code",
    "fist_name" : "first name",
    "last_name" : "last name",
    "phone" : "PHONE"
  }'
```

## HTTP Request

`POST /risk/`

### The parameters are defined as follows

| Parameter      | Default                         | Description                               |
| -------------- | ------------------------------- | ----------------------------------------- |
| `email`        | required                        | Email address to calculate score against. |
| `ip`           | required                        | IP address to calculate score against     |
| `country_code` | optional - strongly recommended | Person’s two letter country code          |
| `fist_name`    | optional - strongly recommended | Person’s first name                       |
| `last_name`    | optional - strongly recommended | Person’s last name                        |
| `phone`        | optional - strongly recommended | Phone number to calculate score against   |
| `brower`       | optional - strongly recommended | User-Agent to calculate score against     |

## Response  Objects details

> Full Response

```json

```

| Attribute | Type  | Description |
| --------- | ----- | ----------- |
| `id`      | hash  |
| `live`    | bool  |
| `email`   | array |
| `address` | array |
| `ip`      | array |
| `risk`    | array |
