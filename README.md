# Test JSON Web Key Set Provider

_Do not delete_

## What is this for?

When validating an authentication token (JWT) from a valid Identity Provider (IdP), the service (e.g. a Stash Data Service) must
first fetch the public keys from the JSON Web Key Set (JWKS).

In testing this is a bit tricky as we generate our own tokens inside the test suite.
So, to validate the URL of this repo is set as the JWKS url.

## Files

Only one file is stored in this repo and that is `.well-known/jwks.json`.
