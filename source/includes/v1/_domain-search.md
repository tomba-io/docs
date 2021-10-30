# Domain Search

Search emails are based on the website
You give one domain name and it returns all the email addresses found on the internet.

```shell
curl --request GET \
  --url 'https://api.tomba.io/v1/domain-search/stripe.com' \
  --header 'Content-Type: application/json' \
  --header 'X-Tomba-Key: ta_xxxx' \
  --header 'X-Tomba-Secret: ts_xxxx'
```

```php
use Tomba\Client;
use Tomba\Services\Domain;

$client = new Client();

$client
    ->setKey('ta_xxxx') // Your API Key
    ->setSecret('ts_xxxx') // Your Secret
;

$domain = new Domain($client);

$result = $domain->domainSearch('stripe.com');

```

```python
from tomba.client import Client
from tomba.services.domain import Domain

client = Client()

(client
  .set_key('ta_xxxx') # Your Key
  .set_secret('') # Your Secret
)

domain = Domain(client)

result = domain.domain_search('stripe.com')

```

```javascript
const tomba = require('tomba');

// Init Tomba
let client = new tomba.Client();

let domain = new tomba.Domain(client);

client
  .setKey("ta_xxxx") // Your Key
  .setSecret("ts_xxxx"); // Your Secret
;

let result = domain.domainSearch('stripe.com');

result
  .then((response) => {
    console.log(response);
  })
  .catch((err) => {
    console.log(err);
  });
```

```ruby
require 'tomba'

client = Tomba::Client.new()

client
    .set_key('ta_xxxx') # Your Key
    .set_secret('ts_xxxx') # Your Secret
;

domain = Tomba::Domain.new(client);

response = domain.domain_search(domain: 'stripe.com');

puts response

```

```java
import io.tomba.api.Tomba;

```

```r
client <- Tomba(key="ta_xxxx",secret="ts_xxxx")
data <- domain_search(client, domain="tomba.io")
data

```

```dart
import 'package:tomba/tomba.dart';

void main() { 
  // Init SDK
  Client client = Client();
  Domain domain = Domain(client);

  client
   .setKey("ta_xxxx") // Your Key
   .setSecret("ts_xxxx"); // Your Secret
  ;

  Future result = domain.domainSearch(
    domain: 'stripe.com',
  );

  result
    .then((response) {
      print(response);
    }).catchError((error) {
      print(error.response);
  });
}

```

```powershell

```

## HTTP Request

`GET /domain-search/:domain`

### The parameters are defined as follows

| Parameter    | Default  | Description                                                                                            |
| ------------ | -------- | ------------------------------------------------------------------------------------------------------ |
| `domain`     | Required | Domain name from which you want to find the email addresses. For example, "stripe.com".                |
| `page`       | optional | Specifies the number of email addresses to skip. The default is 1.                                     |
| `limit`      | optional | Specifies the max number of email addresses to return. The default is 10. valid number(`10`,`20`,`50`) |
| `department` | optional | Get only email addresses for people working in the selected department(s).                             |
| `type`       | optional | Get only `personal` or `generic` email addresses.                                                      |

## Response Objects details

> Full Response

```json
{
    "data": {
        "organization": {
            "location": {
                "country": "US",
                "city": "San Francisco",
                "state": "California",
                "street_address": null
            },
            "social_links": {
                "twitter_url": "https:\/\/twitter.com\/stripe",
                "facebook_url": "https:\/\/www.facebook.com\/StripeHQ",
                "linkedin_url": "https:\/\/www.linkedin.com\/company\/2135371"
            },
            "disposable": false,
            "webmail": false,
            "website_url": "stripe.com",
            "phone_number": "",
            "industries": "internet",
            "postal_code": "94107",
            "employee_count": 976,
            "last_updated": "2021-01-09T05:51:19+01:00",
            "revenue": "150000",
            "accept_all": false,
            "pattern": "{first}",
            "domain_score": 30,
            "organization": "stripe"
        },
        "emails": [
            {
                "email": "nonprofit@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "generic",
                "country": null,
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 55,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-01-22T13:01:41+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/donatetools.com\/pricing",
                        "extracted_on": "2020-12-15 14:35:50",
                        "last_seen_on": "2021-01-22 13:01:41",
                        "still_on_page": true,
                        "website_url": "donatetools.com"
                    },
                    {
                        "uri": "https:\/\/fundrazr.com\/pages\/stripe",
                        "extracted_on": "2020-12-25 09:33:19",
                        "last_seen_on": "2021-01-30 16:21:18",
                        "still_on_page": true,
                        "website_url": "fundrazr.com"
                    },
                    {
                        "uri": "https:\/\/www.wizevents.com\/pricing",
                        "extracted_on": "2020-12-26 07:19:54",
                        "last_seen_on": "2021-01-28 15:43:44",
                        "still_on_page": true,
                        "website_url": "www.wizevents.com"
                    },
                    {
                        "uri": "https:\/\/bloomerang.co\/features\/payment-processing\/",
                        "extracted_on": "2020-12-16 08:14:17",
                        "last_seen_on": "2021-01-29 13:37:40",
                        "still_on_page": true,
                        "website_url": "bloomerang.co"
                    },
                    {
                        "uri": "https:\/\/mancloud.eu\/nl\/hotel-software\/betaaloplossing",
                        "extracted_on": "2021-01-12 14:06:03",
                        "last_seen_on": "2021-02-01 12:48:59",
                        "still_on_page": true,
                        "website_url": "mancloud.eu"
                    },
                    {
                        "uri": "https:\/\/mancloud.eu\/en\/hotel-software\/payment-provider",
                        "extracted_on": "2021-01-12 14:06:14",
                        "last_seen_on": "2021-02-01 12:49:00",
                        "still_on_page": true,
                        "website_url": "mancloud.eu"
                    },
                    {
                        "uri": "https:\/\/donorbox.org\/pricing",
                        "extracted_on": "2020-12-23 13:44:27",
                        "last_seen_on": "2021-02-01 13:15:44",
                        "still_on_page": true,
                        "website_url": "donorbox.org"
                    },
                    {
                        "uri": "https:\/\/rootfunding.com\/blogs\/discounted-stripe-credit-card-processing-fees-for-non-profits",
                        "extracted_on": "2021-01-26 08:55:14",
                        "last_seen_on": "2021-02-01 18:22:06",
                        "still_on_page": true,
                        "website_url": "rootfunding.com"
                    },
                    {
                        "uri": "https:\/\/rootfunding.com\/feed.rss",
                        "extracted_on": "2021-01-26 08:55:15",
                        "last_seen_on": "2021-02-01 18:22:06",
                        "still_on_page": true,
                        "website_url": "rootfunding.com"
                    }
                ]
            },
            {
                "email": "conduct@stripe.com",
                "first_name": "",
                "last_name": "",
                "full_name": null,
                "phone_number": null,
                "type": "personal",
                "country": null,
                "position": null,
                "department": "0",
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 50,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-04-07T19:50:30+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/xpotoursandtravel.com\/vendor\/stripe\/stripe-php\/CODE_OF_CONDUCT.md",
                        "extracted_on": "2021-03-30 14:57:17",
                        "last_seen_on": "2021-04-07 19:50:30",
                        "still_on_page": true,
                        "website_url": "xpotoursandtravel.com"
                    }
                ]
            },
            {
                "email": "am@stripe.com",
                "first_name": "amy",
                "last_name": "mente",
                "full_name": "Amy Mente",
                "phone_number": null,
                "type": "generic",
                "country": "US",
                "position": "Account Support",
                "department": "marketing",
                "seniority": "junior",
                "twitter": null,
                "linkedin": "https:\/\/www.linkedin.com\/in\/amy-mente-6b0854ba",
                "accept_all": false,
                "pattern": "{first}",
                "score": 90,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-03-13T01:43:04+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/chicobetas.com\/alumni-association\/alumni-directory\/",
                        "extracted_on": "2020-12-10 16:39:31",
                        "last_seen_on": "2021-01-22 03:13:01",
                        "still_on_page": true,
                        "website_url": "chicobetas.com"
                    }
                ]
            },
            {
                "email": "notices@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "personal",
                "country": null,
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 50,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-01-29T23:42:02+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/www.swiftcomply.com\/privacy-policy\/",
                        "extracted_on": "2021-01-05 04:20:27",
                        "last_seen_on": "2021-01-27 10:04:44",
                        "still_on_page": true,
                        "website_url": "www.swiftcomply.com"
                    }
                ]
            },
            {
                "email": "julia@stripe.com",
                "first_name": "julia",
                "last_name": "evans",
                "full_name": "Julia Evans",
                "phone_number": null,
                "type": "personal",
                "country": "CA",
                "position": "software engineer",
                "department": "software",
                "seniority": "senior",
                "twitter": null,
                "linkedin": "https:\/\/www.linkedin.com\/in\/jvans",
                "accept_all": false,
                "pattern": "{first}",
                "score": 90,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-03-13T02:00:47+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/pypi.org\/project\/topmodel\/",
                        "extracted_on": "2021-01-30 07:57:41",
                        "last_seen_on": "2021-02-05 03:12:19",
                        "still_on_page": true,
                        "website_url": "pypi.org"
                    }
                ]
            },
            {
                "email": "dpo@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "generic",
                "country": null,
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 65,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-01-12T09:21:07+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/capotinas.com\/politica-de-privacidad\/",
                        "extracted_on": "2021-01-12 09:21:07",
                        "last_seen_on": "2021-01-12 09:21:07",
                        "still_on_page": true,
                        "website_url": "capotinas.com"
                    },
                    {
                        "uri": "https:\/\/consultoriablogger.com\/politica-de-privacidad\/",
                        "extracted_on": "2021-01-14 03:14:51",
                        "last_seen_on": "2021-01-14 03:14:51",
                        "still_on_page": true,
                        "website_url": "consultoriablogger.com"
                    },
                    {
                        "uri": "https:\/\/lorukoru.fi\/pages\/terms-and-conditions",
                        "extracted_on": "2021-01-16 13:49:33",
                        "last_seen_on": "2021-01-16 13:49:33",
                        "still_on_page": true,
                        "website_url": "lorukoru.fi"
                    },
                    {
                        "uri": "https:\/\/leoclub-muenchen-maximilianeum.de\/datenschutz-impressum\/",
                        "extracted_on": "2020-12-05 08:00:11",
                        "last_seen_on": "2021-01-31 04:32:11",
                        "still_on_page": true,
                        "website_url": "leoclub-muenchen-maximilianeum.de"
                    },
                    {
                        "uri": "https:\/\/ochimanikia.com\/politica-de-privacidad\/",
                        "extracted_on": "2020-12-11 02:22:32",
                        "last_seen_on": "2021-01-23 19:24:34",
                        "still_on_page": true,
                        "website_url": "ochimanikia.com"
                    },
                    {
                        "uri": "https:\/\/plusdeprotection.com\/politique-de-confidentialite\/",
                        "extracted_on": "2020-12-06 02:36:03",
                        "last_seen_on": "2021-01-23 19:55:52",
                        "still_on_page": true,
                        "website_url": "plusdeprotection.com"
                    },
                    {
                        "uri": "https:\/\/online-hebamme.com\/datenschutzbestimmungen\/",
                        "extracted_on": "2020-12-10 15:55:57",
                        "last_seen_on": "2021-01-23 20:24:07",
                        "still_on_page": true,
                        "website_url": "online-hebamme.com"
                    },
                    {
                        "uri": "https:\/\/ridelifestyle4home.com\/pages\/conditions-generales-de-vente",
                        "extracted_on": "2020-12-16 21:34:36",
                        "last_seen_on": "2021-01-24 06:35:17",
                        "still_on_page": true,
                        "website_url": "ridelifestyle4home.com"
                    },
                    {
                        "uri": "https:\/\/trouvezmoi.ch\/declaration-de-confidentialite\/",
                        "extracted_on": "2020-12-15 16:18:12",
                        "last_seen_on": "2021-01-24 21:12:22",
                        "still_on_page": true,
                        "website_url": "trouvezmoi.ch"
                    },
                    {
                        "uri": "https:\/\/gaudinfancia.com\/politica-de-privacidad\/",
                        "extracted_on": "2020-12-21 01:02:14",
                        "last_seen_on": "2021-01-25 13:47:29",
                        "still_on_page": true,
                        "website_url": "gaudinfancia.com"
                    },
                    {
                        "uri": "https:\/\/gaudinfancia.com\/ca\/politica-de-privacidad\/",
                        "extracted_on": "2020-12-21 01:03:09",
                        "last_seen_on": "2021-01-25 13:47:30",
                        "still_on_page": true,
                        "website_url": "gaudinfancia.com"
                    },
                    {
                        "uri": "https:\/\/www.rentchester.com\/politica-privacidad\/",
                        "extracted_on": "2020-12-24 18:40:55",
                        "last_seen_on": "2021-01-27 15:26:43",
                        "still_on_page": true,
                        "website_url": "www.rentchester.com"
                    },
                    {
                        "uri": "https:\/\/www.rentchester.com\/politica-de-cookies\/",
                        "extracted_on": "2020-12-24 18:40:57",
                        "last_seen_on": "2021-01-27 15:26:43",
                        "still_on_page": true,
                        "website_url": "www.rentchester.com"
                    },
                    {
                        "uri": "https:\/\/involic.com\/privacy-policy.html",
                        "extracted_on": "2021-01-02 18:23:47",
                        "last_seen_on": "2021-01-28 19:50:39",
                        "still_on_page": true,
                        "website_url": "involic.com"
                    },
                    {
                        "uri": "https:\/\/almarc.de\/datenschutz.htm",
                        "extracted_on": "2020-12-13 02:48:11",
                        "last_seen_on": "2021-01-29 03:53:22",
                        "still_on_page": true,
                        "website_url": "almarc.de"
                    },
                    {
                        "uri": "https:\/\/www.boc-group.com\/en\/privacy-policy\/",
                        "extracted_on": "2020-12-21 15:11:48",
                        "last_seen_on": "2021-01-29 17:18:20",
                        "still_on_page": true,
                        "website_url": "www.boc-group.com"
                    },
                    {
                        "uri": "https:\/\/www.drivelock.com\/data-protection",
                        "extracted_on": "2020-12-13 06:16:37",
                        "last_seen_on": "2021-01-31 14:32:44",
                        "still_on_page": true,
                        "website_url": "www.drivelock.com"
                    },
                    {
                        "uri": "https:\/\/www.drivelock.com\/fr\/protection-des-donnees",
                        "extracted_on": "2020-12-13 06:17:00",
                        "last_seen_on": "2021-01-31 14:32:45",
                        "still_on_page": true,
                        "website_url": "www.drivelock.com"
                    },
                    {
                        "uri": "https:\/\/www.drivelock.de\/datenschutz\/",
                        "extracted_on": "2020-12-13 06:17:15",
                        "last_seen_on": "2021-01-31 14:32:45",
                        "still_on_page": true,
                        "website_url": "www.drivelock.de"
                    },
                    {
                        "uri": "https:\/\/actuanimaux.com\/actuanimaux\/cgu-stripe\/",
                        "extracted_on": "2020-12-13 16:08:48",
                        "last_seen_on": "2021-01-31 19:08:52",
                        "still_on_page": true,
                        "website_url": "actuanimaux.com"
                    }
                ]
            },
            {
                "email": "site@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "generic",
                "country": null,
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 50,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-02-26T21:12:52+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/atelim.com\/this-week-is-going-to-be-huge-for-ritual-sacrifices.html?part=17",
                        "extracted_on": "2021-02-17 23:57:41",
                        "last_seen_on": "2021-02-26 21:12:52",
                        "still_on_page": true,
                        "website_url": "atelim.com"
                    }
                ]
            },
            {
                "email": "support@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "generic",
                "country": "US",
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 75,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-01-16T00:17:41+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/www.hsi-medical.com\/datenschutz\/",
                        "extracted_on": "2021-01-16 00:17:41",
                        "last_seen_on": "2021-01-16 00:17:41",
                        "still_on_page": true,
                        "website_url": "www.hsi-medical.com"
                    },
                    {
                        "uri": "https:\/\/knucklewalkgym.com\/terms\/",
                        "extracted_on": "2021-01-16 04:16:49",
                        "last_seen_on": "2021-01-16 04:16:49",
                        "still_on_page": true,
                        "website_url": "knucklewalkgym.com"
                    },
                    {
                        "uri": "https:\/\/www.nyccfb.info\/PDF\/NYC-Votes_FAQ.pdf",
                        "extracted_on": "2021-01-19 20:52:05",
                        "last_seen_on": "2021-01-19 20:52:05",
                        "still_on_page": true,
                        "website_url": "www.nyccfb.info"
                    },
                    {
                        "uri": "https:\/\/chitachok.ru\/forums\/288\/",
                        "extracted_on": "2020-12-18 06:27:46",
                        "last_seen_on": "2021-01-22 05:52:27",
                        "still_on_page": true,
                        "website_url": "chitachok.ru"
                    },
                    {
                        "uri": "https:\/\/www.enzocouture.us\/index.php?id_cms=5&controller=cms&id_lang=1",
                        "extracted_on": "2020-12-15 14:58:03",
                        "last_seen_on": "2021-01-22 18:02:55",
                        "still_on_page": true,
                        "website_url": "www.enzocouture.us"
                    },
                    {
                        "uri": "https:\/\/www.listedbeauty.com\/stripe_info",
                        "extracted_on": "2020-12-10 00:26:59",
                        "last_seen_on": "2021-01-23 12:07:37",
                        "still_on_page": true,
                        "website_url": "www.listedbeauty.com"
                    },
                    {
                        "uri": "https:\/\/online-theatre-academy.com\/privacy-policy\/",
                        "extracted_on": "2020-12-11 00:31:35",
                        "last_seen_on": "2021-01-23 20:29:12",
                        "still_on_page": true,
                        "website_url": "online-theatre-academy.com"
                    },
                    {
                        "uri": "https:\/\/online-theatre-academy.com\/ru\/privacy-policy\/",
                        "extracted_on": "2020-12-11 00:35:02",
                        "last_seen_on": "2021-01-23 20:29:12",
                        "still_on_page": true,
                        "website_url": "online-theatre-academy.com"
                    },
                    {
                        "uri": "https:\/\/online-theatre-academy.com\/de\/privacy-policy\/",
                        "extracted_on": "2020-12-11 00:35:25",
                        "last_seen_on": "2021-01-23 20:29:12",
                        "still_on_page": true,
                        "website_url": "online-theatre-academy.com"
                    },
                    {
                        "uri": "https:\/\/www.pregfit.de\/datenschutzerklaerung?utm_source=pregfit&utm_medium=home&utm_campaign=1&utm_content=12",
                        "extracted_on": "2020-12-13 09:28:50",
                        "last_seen_on": "2021-01-24 01:17:57",
                        "still_on_page": true,
                        "website_url": "www.pregfit.de"
                    },
                    {
                        "uri": "https:\/\/www.pregfit.de\/datenschutzerklaerung",
                        "extracted_on": "2020-12-13 09:28:58",
                        "last_seen_on": "2021-01-24 01:17:57",
                        "still_on_page": true,
                        "website_url": "www.pregfit.de"
                    },
                    {
                        "uri": "https:\/\/stripeexperts.com\/index.php?id_cms=12&controller=cms&id_lang=1",
                        "extracted_on": "2020-12-10 21:08:41",
                        "last_seen_on": "2021-01-24 18:15:16",
                        "still_on_page": true,
                        "website_url": "stripeexperts.com"
                    },
                    {
                        "uri": "https:\/\/boutique-rasta.fr\/pages\/conditions-generales-de-ventes",
                        "extracted_on": "2020-12-20 00:12:13",
                        "last_seen_on": "2021-01-24 19:44:37",
                        "still_on_page": true,
                        "website_url": "boutique-rasta.fr"
                    },
                    {
                        "uri": "https:\/\/llarenapagatu.com\/donatius\/",
                        "extracted_on": "2020-12-26 08:52:15",
                        "last_seen_on": "2021-01-26 23:29:05",
                        "still_on_page": true,
                        "website_url": "llarenapagatu.com"
                    },
                    {
                        "uri": "https:\/\/ludwig.guru\/privacy",
                        "extracted_on": "2020-12-25 18:41:45",
                        "last_seen_on": "2021-01-27 00:22:31",
                        "still_on_page": true,
                        "website_url": "ludwig.guru"
                    },
                    {
                        "uri": "http:\/\/shovler.com\/blog\/how-to-become-a-snow-shoveler-on-shovler\/",
                        "extracted_on": "2020-12-23 05:59:51",
                        "last_seen_on": "2021-01-27 02:51:47",
                        "still_on_page": true,
                        "website_url": "shovler.com"
                    },
                    {
                        "uri": "http:\/\/shovler.com\/blog\/page\/4\/",
                        "extracted_on": "2020-12-23 05:59:51",
                        "last_seen_on": "2021-01-27 02:51:47",
                        "still_on_page": true,
                        "website_url": "shovler.com"
                    },
                    {
                        "uri": "http:\/\/shovler.com\/blog\/2016\/11\/",
                        "extracted_on": "2020-12-23 05:59:53",
                        "last_seen_on": "2021-01-27 02:51:47",
                        "still_on_page": true,
                        "website_url": "shovler.com"
                    },
                    {
                        "uri": "https:\/\/gigsmart.com\/terms\/",
                        "extracted_on": "2021-01-02 08:51:21",
                        "last_seen_on": "2021-01-27 13:22:21",
                        "still_on_page": true,
                        "website_url": "gigsmart.com"
                    },
                    {
                        "uri": "https:\/\/zkorean.com\/account\/register",
                        "extracted_on": "2021-01-03 18:38:20",
                        "last_seen_on": "2021-01-27 19:34:49",
                        "still_on_page": true,
                        "website_url": "zkorean.com"
                    }
                ]
            },
            {
                "email": "jsmith@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "personal",
                "country": null,
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 50,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-02-02T16:57:52+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/www.lusha.com\/organization\/stripe_26094\/",
                        "extracted_on": "2021-01-31 03:55:22",
                        "last_seen_on": "2021-02-26 16:45:53",
                        "still_on_page": true,
                        "website_url": "www.lusha.com"
                    }
                ]
            },
            {
                "email": "smith@stripe.com",
                "first_name": null,
                "last_name": null,
                "full_name": null,
                "phone_number": null,
                "type": "personal",
                "country": null,
                "position": null,
                "department": null,
                "seniority": null,
                "twitter": null,
                "linkedin": null,
                "accept_all": false,
                "pattern": "{first}",
                "score": 50,
                "verification": {
                    "date": null,
                    "status": null
                },
                "last_updated": "2021-02-02T16:57:52+01:00",
                "sources": [
                    {
                        "uri": "https:\/\/www.lusha.com\/organization\/stripe_26094\/",
                        "extracted_on": "2021-01-31 03:55:22",
                        "last_seen_on": "2021-02-26 16:45:53",
                        "still_on_page": true,
                        "website_url": "www.lusha.com"
                    }
                ]
            }
        ]
    },
    "meta": {
        "total": 1514,
        "pageSize": 10,
        "current": 0,
        "total_pages": 152
    }
}
```

| Attribute                                    | Type   | Description                           |
| -------------------------------------------- | ------ | ------------------------------------- |
| `organization` > `location.country`          | string | The country of company                |
| `organization` > `social_links.twitter_url`  | string | The Twitter screen name               |
| `organization` > `social_links.facebook_url` | string | The Facebook screen name              |
| `organization` > `social_links.linkedin_url` | string | The Linkedin screen name              |
| `organization` > `disposable`                | bool   | is disposable email service           |
| `organization` > `webmail`                   | bool   | is webmail email                      |
| `organization` > `website_url`               | string | The Domain of company’s website       |
| `organization` > `state`                     | string | The company state                     |
| `organization` > `accept_all`                | bool   | The SMTP checks                       |
| `organization` > `industries`                | string | The company industries info           |
| `organization` > `last_updated`              | date   | The time at which we update this data |
| `organization` > `organization`              | string | The Name of company                   |
| `organization` > `pattern`                   | string | The Name of company                   |
| `emails`                                     | array  | The list of Emails                    |
