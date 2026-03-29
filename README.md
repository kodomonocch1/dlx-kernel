# DLX Public Evaluator Kit

This repo is the public evaluator kit for a narrow auditable execution surface. It is a static, public-facing hub for evaluators who need to understand the current managed execution endpoint, review the workflow insurance / reliability layer, and decide whether to submit one payload for review.

The evaluator flow is intentionally narrow. A submission is first accepted, then it resolves to either `succeeded` or `failed_safe`. That framing matters: the public kit is about verified result or safe failure at the workflow boundary, not optimistic completion or broad product claims.

Use the static pages here to move through the current evaluator path. Start at the [public evaluator kit home](./index.html), then review the [quickstart](./quickstart.html), inspect the [receipt viewer](./receipt-viewer.html), estimate downstream cost with the [ROI calculator](./roi-calculator.html), or use the [submit payload page](./submit-payload.html) when you are ready to share one workflow payload in a narrow intake flow.

This repo is public-facing only. It is not the private DLX kernel implementation, it does not expose backend code, and it does not define new runtime or product capabilities beyond the current evaluator kit surface.

Contact: [tetsutetsu11@icloud.com](mailto:tetsutetsu11@icloud.com)

## How To Engage

- request an evaluation API key
- submit one payload
- open a discussion
- open an issue if you want to share a payload in structured form

## Community Routing

Use the short routing note in [docs/community-routing.md](./docs/community-routing.md) to decide when to use Discussions, Issues, email, or the submit payload page.
