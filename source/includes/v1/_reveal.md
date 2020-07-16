# Reveal API

Our Reveal API takes an IP address, and returns the company associated with that IP. This is especially useful for de-anonymizing traffic on your website, analytics, and customizing landing pages for specific company verticals.

Powering Reveal is a unique dataset that combines both public and proprietary sources to give you an insight into the companies visiting your website whatever their size, even if they don’t have their own public ASN block.

Currently we do not support `IPv6` addresses, only `IPv4` addresses.

## Lookup IP addresses

To use the Reveal API, send us an IP address and we’ll return the company domain and information associated. If we can’t match the IP to a company, we’ll return a `404` HTTP status instead of a `200`.
