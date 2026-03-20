# Webhook Flow

## Why Webhooks Exist

The gateway is accepted-first. Webhooks are optional for evaluation. Polling `GET /v1/executions/:id` is a valid evaluator path.

## Webhook Test Endpoint

For webhook-boundary evaluation, the current public test path is:

- `POST /v1/webhooks/test`

Confirmed latest response:

```json
{
  "accepted": true,
  "eventId": "exec_mmz8xzls_8gr5jxyq",
  "targetUrl": "https://webhook.site/af214b59-a05d-431f-9d81-e4706a6a3e96",
  "eventType": "gateway.delivery.test",
  "receivedAt": "2026-03-20T18:42:40.384Z",
  "deliveryState": "delivered"
}
```

## Observed Webhook Payload

Confirmed observed payload from the webhook target:

```json
{
  "eventId": "exec_mmz8xzls_8gr5jxyq",
  "eventType": "gateway.delivery.test",
  "deliveredAt": "2026-03-20T18:42:40.384Z",
  "payload": {
    "probe": "phase1-demo"
  }
}
```

## Important Boundary

- webhook is not required for evaluation
- polling remains the simplest path for evaluating terminal states
- execution terminal states remain `succeeded` and `failed_safe`
- webhook delivery state is a delivery concern, not a replacement for workflow outcome truth

## Trust Artifact Reference

If you need to explain why the workflow can be trusted after completion, link evaluators to:

- `index.html`
- `receipt-viewer.html`
