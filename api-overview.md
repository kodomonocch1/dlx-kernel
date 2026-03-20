# API Overview

## Scope

This is the smallest useful public evaluator view of the current Auditable Execution Gateway surface.

## Request Example

```json
{
  "input": {
    "text": "phase1-success"
  },
  "outputContract": "contract:extract.result.v1",
  "budget": {
    "maximumEu": 1,
    "reserveEu": 1
  },
  "idempotencyKey": "eval-request-001",
  "webhookUrl": "https://example.com/dlx/webhook"
}
```

## Accepted-First Behavior

`POST /v1/executions/extract` accepts work first. It does not claim that the workflow is already complete.

Example acceptance response:

```json
{
  "executionId": "exec_mmz8xtgp_h5pael2y",
  "workflowId": "wf_mmz8xtgp_shoocoiz",
  "status": "accepted",
  "acceptedAt": "2026-03-20T18:42:32.425Z",
  "pollUrl": "/v1/executions/exec_mmz8xtgp_h5pael2y"
}
```

`pollUrl` is relative. Resolve it against the gateway base URL you are evaluating.

## Success Response Example

```json
{
  "executionId": "exec_mmz8xtgp_h5pael2y",
  "workflowId": "wf_mmz8xtgp_shoocoiz",
  "status": "succeeded",
  "workflowStatus": "delivery_recorded",
  "finalOutput": {
    "result": "phase1-success",
    "status": "complete"
  },
  "deliveryState": "recorded"
}
```

## Failed-Safe Response Example

```json
{
  "executionId": "exec_mmz8xw6e_zyhx6twm",
  "workflowId": "wf_mmz8xw6e_xvcyb99x",
  "status": "failed_safe",
  "workflowStatus": "delivery_recorded",
  "safeFailure": {
    "failureClassification": "schema_failure"
  },
  "deliveryState": "recorded"
}
```

## Interpretation

- `succeeded` means deterministic validation passed.
- `failed_safe` means the workflow stopped without claiming unvalidated success.
- `deliveryState` describes notification handling, not business outcome truth.
- the latest confirmed live success and failed_safe runs both ended with `deliveryState: "recorded"`

## Static Path

- `index.html`
- `webhook-flow.html`
- `receipt-viewer.html`

## Trust Artifact Reference

For the current static evaluator kit, use `receipt-viewer.html` as the public-safe trust artifact entry point.
