# Publishing The Evaluator Kit

## Scope

The publishable static path is the `docs/public/` directory.

Canonical entry page:

- `docs/public/index.html`

Supporting files:

- `docs/public/kit.css`
- `docs/public/quickstart.html`
- `docs/public/api-overview.html`
- `docs/public/webhook-flow.html`
- `docs/public/roi-calculator.html`
- `docs/public/receipt-viewer.html`

## No-Build Option

This kit is static. No backend or build system is required.

To publish it, expose the entire `docs/public/` directory from any static file host.

## Local Preview

Two simple options:

1. Open `docs/public/index.html` directly in a browser.
2. Serve `docs/public/` from a basic local static server if you want normal relative-URL behavior.

## Publishing Rule

Publish the whole folder, not just one file, so the navigation and stylesheet stay intact.

## Scope Boundary

This publishing note is only for the evaluator kit. It does not add new runtime endpoints, hosting dashboards, or product capabilities.
