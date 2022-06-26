# Enrichment

The Enrichment API lets you look up person and company data based on an email, For example, you could retrieve a person’s name, location and social handles from an email

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/enrich?email=b.mohamed@tomba.io' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

## HTTP Request

`GET /enrich/?email=b.mohamed@tomba.io`

### The parameters are defined as follows

| Parameter | Default  | Description                      |
| --------- | -------- | -------------------------------- |
| `email`   | Required | The email address to find data . |

## Response Objects details

> Full Response

```json
{
  "data": {
    "website_url": "tomba.io",
    "accept_all": null,
    "email": "b.mohamed@tomba.io",
    "first_name": "Mohamed",
    "last_name": "Ben rebia",
    "country": "DZ",
    "gender": "male",
    "phone_number": null,
    "position": "CEO",
    "twitter": null,
    "linkedin": "https:\/\/www.linkedin.com\/in\/mohamed-ben-rebia-4337061ba",
    "disposable": false,
    "webmail": false,
    "full_name": "Mohamed Ben rebia",
    "company": "Tomba technology web service LLC ",
    "score": 99,
    "verification": {
      "date": "2021-05-25",
      "status": "valid"
    },
    "sources": [{
        "uri": "https:\/\/github.com\/tomba-io\/generic-emails\/blob\/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9\/src\/lib\/validation\/hash.ts",
        "website_url": "github.com",
        "extracted_on": "2021-02-08T20:09:54+01:00",
        "last_seen_on": "2021-02-08T22:43:40+01:00",
        "still_on_page": true
      }, {
        "uri": "https:\/\/github.com\/tomba-io\/generic-emails\/blame\/084fc1a63d3cdaf9a34f255bedc2baea49a8e8b9\/src\/lib\/validation\/hash.ts",
        "website_url": "github.com",
        "extracted_on": "2021-02-08T20:09:59+01:00",
        "last_seen_on": "2021-02-08T22:43:40+01:00",
        "still_on_page": true
      }
      ....
      ....
      ....
    ]
  }
}
```

| Attribute      | Type   | Description                                                                                                                |
| -------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `email`        | string | The email address                                                                                                          |
| `website_url`  | string | Company domain                                                                                                             |
| `first_name`   | string | First name of person                                                                                                       |
| `last_name`    | string | Last name of person                                                                                                        |
| `full_name`    | string | Full formatted name of person. Sometimes this will be present even if the `last_name` or `first_name` aren’t available     |
| `country`      | string | Two letter country code based on location                                                                                  |
| `accept_all`   | bool   | is `true` if the SMTP server accepts all the email addresses. It means you can have have `false` positives on SMTP checks. |
| `position`     | string | The job title of person (if found)                                                                                         |
| `twitter`      | string | Twitter handle for the person (if found).                                                                                  |
| `linkedin_url` | string | LinkedIn URL for the person (if found).                                                                                    |
| `phone_number` | bool   | true (if found)                                                                                                            |
| `company`      | string | The company of person (if found)                                                                                           |
