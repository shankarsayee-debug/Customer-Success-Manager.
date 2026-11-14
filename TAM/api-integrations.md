# API Engineering, Integrations and Webhooks

## Typical request path
Client → DNS/TLS/network → API endpoint → authentication/authorization → application service → data/downstream service → response or webhook callback.

## Technical discovery
Capture business objective; source/destination systems; Dev/UAT/Prod environments; API style/version/specification; endpoint, method and payload schema; authentication/scopes/redirect URI/PKCE; data mapping and identifiers; sync/async behavior; polling, callbacks, retries and idempotency; throughput, concurrency, rate limits and timeouts; monitoring, logs, errors, versioning, SLA and support ownership; sandbox, UAT and go-live criteria.

## HTTP troubleshooting
2xx indicates protocol-level success, not necessarily business completion. For 4xx inspect request validity, authentication, authorization, validation and rate limits. For 5xx inspect service/dependency failures and server logs. If no HTTP response exists, investigate DNS, TCP, TLS, proxy and timeout layers. Compare a known-good request with a failing one; capture method, endpoint, status, response, timestamp, timezone and correlation ID. Redact secrets and personal data.

## Webhooks
An API request is client-initiated; a webhook is an event notification sent to a registered callback URL. Verify URL/TLS reachability, event subscription, signature verification, acknowledgement, retry/backoff, delivery history and idempotent processing.

## CORS and idempotency
For browser failures inspect Console and Network, including OPTIONS preflight. Validate allowed origins, methods, headers and credentials. CORS does not replace server-side authorization. Before retrying an operation, determine whether it may already have completed and whether a repeat can create duplicate side effects. Use only documented idempotency support.

## Notion references
- [API Authentication Best Practices](https://app.notion.com/p/37b5a0f10ce480ed87e3cd5ccf93fce5)
- [API Known Issues](https://app.notion.com/p/3fc5a0f10ce480b1bf1ef5c4fcf9439d)
- [CORS Preflight](https://app.notion.com/p/3fc5a0f10ce480a4a367c78b0d3bb364)
- [Webhooks implementation](https://app.notion.com/p/37b5a0f10ce480188186fa5eca0f2fc4)
- [Webhooks troubleshooting](https://app.notion.com/p/3fc5a0f10ce48068a55ae3f3df938c78)
- [Idempotency and Reliability](https://app.notion.com/p/3fe5a0f10ce48011856ff320ac792341)
