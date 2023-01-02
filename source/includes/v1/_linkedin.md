# Linkedin Finder

This API endpoint generates or retrieves the most likely email address from a Linkedin URL.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/linkedin?url=https://www.linkedin.com/in/alex-maccaw-ab592978' \
  --header 'content-type: application/json' \
  --header 'X-Tomba-Key: xxxxxxxxxxxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

## HTTP Request

`GET /linkedin?url=:url`

### The parameters are defined as follows

| Parameter | Default  | Description                                                                                               |
| --------- | -------- | --------------------------------------------------------------------------------------------------------- |
| url       | Required | The URL of the Linkedin.  For example, "https://clearbit.com/blog/company-name-to-domain-api". |

## Response Objects details

> Full Response

```json
{
  "data": {
    "website_url": "clearbit.com",
    "accept_all": true,
    "email": "alex@clearbit.com",
    "first_name": "Alex",
    "last_name": "Maccaw",
    "country": "US",
    "gender": "male",
    "phone_number": null,
    "position": "founder",
    "twitter": "https://twitter.com/maccman",
    "linkedin": "https://www.linkedin.com/in/alex-maccaw-ab592978",
    "disposable": false,
    "webmail": false,
    "full_name": "Alex Maccaw",
    "company": "Clearbit",
    "score": 90,
    "verification": {
      "date": null,
      "status": null
    },
    "sources": [
      {
        "uri": "https://pypi.org/project/clearbit/",
        "website_url": "pypi.org",
        "extracted_on": "2021-01-29T20:32:08+01:00",
        "last_seen_on": "2021-02-05T02:15:43+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://growjo.com/company/Clearbit",
        "website_url": "growjo.com",
        "extracted_on": "2021-07-23T09:11:15+01:00",
        "last_seen_on": "2021-07-23T20:19:38+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://pdfcookie.com/documents/book1xlsx-025ekom5x721",
        "website_url": "pdfcookie.com",
        "extracted_on": "2021-10-01T14:53:49+01:00",
        "last_seen_on": "2021-10-03T00:55:58+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://github.com/clearbit/clearbit-ruby/blob/master/clearbit.gemspec",
        "website_url": "github.com",
        "extracted_on": "2021-12-22T15:54:30+01:00",
        "last_seen_on": "2021-12-23T00:12:25+01:00",
        "still_on_page": true
      },
      {
        "uri": "https://github.com/clearbit/clearbit-python",
        "website_url": "github.com",
        "extracted_on": "2021-12-22T15:54:33+01:00",
        "last_seen_on": "2021-12-23T00:12:25+01:00",
        "still_on_page": true
      },
      ...
      ...
      ...
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
| `department`   | string | The person working in the selected department(s).                                                                          |
| `twitter`      | string | Twitter handle for the person (if found).                                                                                  |
| `linkedin_url` | string | LinkedIn URL for the person (if found).                                                                                    |
| `phone_number` | bool   | true if found                                                                                                              |
| `company`      | string | The company of person (if found)                                                                                           |
| `last_updated` | string | The time at which we update this data                                                                                      |
