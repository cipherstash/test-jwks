# Test JSON Web Key Set Provider

_Do not delete_

## What is this for?

When validating an authentication token (JWT) from a valid Identity Provider (IdP), the service (e.g. a Stash Data Service) must first fetch the public keys from the JSON Web Key Set (JWKS).

In testing this is a bit tricky as we generate our own tokens inside the test suite.  So, to validate the URL of this repo is set as the JWKS url.

## Files


A `jwks.json` file is publicly accessible at `https://cipherstash.github.io/test-jwks/.well-known./jwks.json`

It stores the JSON Web Key Set for the issuer "https://cipherstash.github.io/test-jwks"

The aforementioned file is used as a JSON Web Key Set in testing the `data-service` in the `platform` repo. It fullfils the role of a "proper" issuer configuration. The coressponding key ID and `.pem` file are managed in the `platform` repo.

The `alt` directory stores alternative issuers (there is just one presently) in order for testing non-happy path cases such as malicious users trying to use fraudulent JWTs. In this case, the issuer URL will be https://cipherstash.github.io/test-jwks/alt/issuer-1.
