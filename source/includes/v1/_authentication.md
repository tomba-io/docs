
## Authentication

Authentication is made with a `key` and `secret` you will have to add to every call you make to our API.
This parameter is always required.
We'll return an error if the key is either missing or invalid.

Your API `key` and `secret` is what identifies your account, so make sure to keep it secret! You can at anytime generate or delete API `keys` on your [dashboard](#dashboard).

| Api      | Authorization | Location |
| -------- | ------------- | -------- |
| `key`    | `X-Tomba-Key` | `header` |
| `secret` | `secret`      | `query`  |
