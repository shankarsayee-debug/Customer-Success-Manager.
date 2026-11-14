# Identity, Authentication and Access Management

## Core concepts
An IdP authenticates the user and issues an assertion/token; an SP or relying party consumes it. OAuth 2.0 is an authorization framework; OIDC adds an identity layer. SAML 2.0 is an XML-based federation protocol. JWT is a token format; validate its signature and claims, not merely decoded contents. JWKS publishes public keys used to verify signed tokens.

## Federated sign-in
User → application/SP → IdP → authentication/MFA → token/assertion → SP validation → session.

## SAML checks
Validate IdP issuer/entity ID, SP entity ID/audience, ACS URL, destination, NameID, required attributes, signature, signing certificate, expiry, clock synchronization, binding and user assignment.

## OAuth/OIDC checks
Validate authorization/token endpoints, client ID, redirect URI, scopes, Authorization Code + PKCE where appropriate, state/nonce, issuer, audience, expiry, signature, JWKS key rotation and refresh-token policy.

## Authentication versus authorization
Authentication establishes identity; authorization determines permitted actions. Successful login does not prove correct role/group/resource access.

## Security
Never put passwords, access/refresh tokens, client secrets, private keys or session cookies in tickets or KB articles. Share redacted traces and only necessary identifiers.

## References
- [OAuth, OIDC and SAML](https://app.notion.com/p/37b5a0f10ce4802bb1e8c89c85ff1dc9)
- [Identity Provider](https://app.notion.com/p/37b5a0f10ce48020be31c7dc474e4cb9)
- [SAML Architecture](https://app.notion.com/p/37b5a0f10ce480b98b76edd2a1e2b960)
- [JWKS Endpoint](https://app.notion.com/p/37d5a0f10ce4807cb0cde674a63a2a1d)
- [RADIUS and MFA](https://app.notion.com/p/3ad5a0f10ce480ecb31dc744298256b9)
