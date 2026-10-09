---
name: servicedesk-plus-create-and-retrieve-request
description: Create a new request and then retrieve its details.
api: openapi/servicedesk-plus-requests-api-openapi.yml
operations:
- createRequest
- getRequest
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/servicedesk-plus-requests-api-openapi.yml ; every operationId checked against the contract
---

# servicedesk-plus-create-and-retrieve-request

Create a new request and then retrieve its details.

## Steps

1. 1. Call `createRequest` with required body fields (e.g., `title`, `description`, `requester_id`).
2. 2. Use the `request_id` returned from `createRequest` to call `getRequest` with path parameter `request_id`.

## Rules

- Auth: Include an `Authorization: Bearer <access_token>` header (OAuth2).
- Idempotency: `createRequest` is not idempotent; repeat calls will create duplicate requests.
