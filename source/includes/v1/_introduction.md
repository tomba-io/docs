# Introduction

The Tomba API is exposed via [RESTful](http://en.wikipedia.org/wiki/Representational_state_transfer) web services and makes use of the standard [JSON](https://en.wikipedia.org/wiki/JSON) encoding.

This documentation will show you how to query.

Three main calls are available:

- The [Domain Search](#aa) returns all the email addresses found using one given domain name, with sources.
- The [Email Finder](#aa) guesses the most likely email of a person using his/her first name, last name and a domain name.
- The [Email Verifier](#aa) checks the deliverability of a given email address, verifies if it has been found in our database, and returns their sources.
- The [Technologies Finder](#aa)
- The [IP address](#aa)
- The [Bulk Domain Search](#aa) Find emails from a list of companies or domains
- The [Bulk Email Finder](#aa) Find emails from a list of name and companies or domains
- The [Bulk Email Verifier](#aa) Verify a list of professional emails at once
- The [Bulk Technologies Finder](#aa) Find domains tools
- The [Bulk IP address](#aa) Find IP address details

> API endpoint

```bash
https://api.tomba.io/v1/
```

> API endpoint
