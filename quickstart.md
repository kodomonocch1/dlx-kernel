# DLX Quickstart

DLX Phase 1 is not raw API access. It is a workflow safety layer for auditable task execution on the current narrow managed workflow surface.

In three minutes, a technical evaluator should understand the current shape:

1. create an execution with `POST /v1/executions/extract`
2. receive an accepted-first response
3. poll `GET /v1/executions/:id` or provide a webhook target
4. reach either validated success or failed_safe
5. review public-safe trust artifacts when needed

## Current Public Surface

- `POST /v1/executions/extract`
- `GET /v1/executions/:id`
- optional webhook delivery for completion notification
- current live evaluation base URL: `https://nurturing-nurturing-production.up.railway.app`

## Minimal Request Example

```bash
curl -X POST https://nurturing-nurturing-production.up.railway.app/v1/executions/extract \
  -H "content-type: application/json" \
  -H "x-api-key: test-key" \
  -d '{
    "input": { "text": "phase1-success" },
    "outputContract": "contract:extract.result.v1",
    "budget": { "maximumEu": 1 },
    "idempotencyKey": "phase1-live-eval-1"
  }'
```

The create response is accepted-first. `pollUrl` is a relative path and should be resolved against the gateway base URL, for example:

- `https://nurturing-nurturing-production.up.railway.app` + `/v1/executions/exec_mmz8xtgp_h5pael2y`

## What You Get

- guaranteed / auditable task execution at the workflow boundary
- a workflow safety layer, not just an LLM call
- validated success or safe failure, not silent optimistic completion
- polling is a valid evaluator path; webhook is optional

## Static Entry

- `index.html`

## Read Next

- `api-overview.html`
- `webhook-flow.html`
- `receipt-viewer.html`

## Public-Safe Assets

- `roi-calculator.html`
- `receipt-viewer.html`

Those pages are static and can be opened locally for screenshots or evaluator walkthroughs.
