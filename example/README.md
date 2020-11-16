# SimpleWebAuthn Example Project

A fully-functional reference implementation of **@simplewebauthn/server** and **@simplewebauthn/browser**.

You can find an in-depth guide to the Example Project here: https://simplewebauthn.dev/docs/advanced/example-project

## FIDO Conformance Tests

The example project acts as a test server for the FIDO Conformance Tools server
test suite.

A complete guide is available on the [Validating FIDO conformance] page of the
docs.

### Validating Unpublished Changes

This section assumes you have obtained the FIDO Conformance Tools application
and loaded the metadata statements as described in the
[Validating FIDO conformance] docs.

First, validate your setup by running conformance tests against the published
package:

```
npm i && npm run start-fido-conformance
# run conformance test
```

Link you modified `@simplewebauthn/server` from the project root:

```
npx lerna exec --scope @simplewebauthn/server npm link
(cd example && npm link @simplewebauthn/server)
# start / restart example server
# run conformance test
```

[validating fido conformance]: https://simplewebauthn.dev/docs/advanced/fido-conformance
