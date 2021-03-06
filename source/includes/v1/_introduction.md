# Introduction

We are maintaining a Public API. This service allows any developers to retrieve and manage TOmba data with HTTP requests.



This documentation will show you how to query.

Twelve main calls are available:

- The [Account information](#account-information) : 
- The [Domain Search](#domain-search) returns all the email addresses found using one given domain name, with sources.
- The [Email Finder](#email-finder) guesses the most likely email of a person using his/her first name, last name and a domain name.
- The [Email Verifier](#email-verifier) checks the deliverability of a given email address, verifies if it has been found in our database, and returns their sources.
- The [Leads.](#leads) .
- The [Leads Lists.](#leads-lists)
- The [Lead Attributes.](#leads-attributes)
- The [Usage.](#usage)
- The Account [Logs.](#logs)
- The [Keys.](#keys)
- The [Email Count.](#email-count) : With this API method, you can find out the number of email addresses from a certain domain
- The [Domain autocomplete.](#autocomplete) : Provides a short reference to the "Autocomplete search" entity type

> API endpoint

```bash
https://api.tomba.io/v1/
```

> API endpoint
