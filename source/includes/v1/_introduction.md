# Introduction

The Tomba API is exposed via [RESTful](http://en.wikipedia.org/wiki/Representational_state_transfer) web services and makes use of the standard [JSON](https://en.wikipedia.org/wiki/JSON) encoding.

This documentation will show you how to query.

Three main calls are available:

- The [Domain Search](#domain-search) returns all the email addresses found using one given domain name, with sources.
- The [Email Finder](#email-finder) guesses the most likely email of a person using his/her first name, last name and a domain name.
- The [Email Verifier](#email-verifier) checks the deliverability of a given email address, verifies if it has been found in our database, and returns their sources.
- The [IP address](#ip-address) checks IP address details.
- The [Leads.](#leads) .
- The [Leads Lists.](#leads-lists)
- The [Lead Attributes.](#leads-attributes)
- The [Usage.](#usage)
- The Account [Logs.](#logs)
- The [Keys.](#keys)
- The [Email Count.](#email-count)
- The [Domain autocomplete.](#autocomplete)

> API endpoint

```bash
https://api.tomba.io/v1/
```

> API endpoint
