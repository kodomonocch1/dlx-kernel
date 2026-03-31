# DLX Kernel

This repository is **not** the current primary public evaluation entry for DLX Phase 1.

The current public-facing evaluation repo is:

- **[dlx-public-kit](https://github.com/kodomonocch1/dlx-public-kit)**

That repo is the correct starting point for external evaluators who want to understand the current Phase 1 surface, review the narrow public flow, and inspect sanitized examples and public-safe verification notes.

---

## What This Repo Is

This repository exists as a **kernel-oriented / legacy public companion** for DLX.

DLX itself is being developed around a long-term kernel-first direction. The current public Phase 1 surface is intentionally narrow and proxy-first, while the deeper kernel and delivery-layer reality sit behind that surface.

In practical terms:

- the current **public entry** is `dlx-public-kit`
- the current **public Phase 1 surface** is a thin MCP-native trust proxy
- the current evaluator-facing operations are intentionally narrow
- the gateway is treated as an **internal / secondary delivery layer**, not the public product face

This repository should therefore be read as background or companion context, not as the primary evaluator path.

---

## Start Here Instead

For the current public Phase 1 evaluation path, start with:

- **[dlx-public-kit](https://github.com/kodomonocch1/dlx-public-kit)**
- `README.md` in that repo
- `docs/quickstart-phase1.md`
- `docs/api-phase1.md`
- `docs/verification-phase1.md`
- `examples/phase1/`

That repo reflects the current public positioning more accurately than this one.

---

## What DLX Phase 1 Currently Means

At the public level, DLX Phase 1 is presented as a **thin MCP-native trust proxy**.

The evaluator-facing logic is intentionally narrow:

- call `extract`
- then call `get_execution`
- judge the boundary by whether work resolves to:
  - `succeeded`
  - `failed_safe`

The public promise is not a broad workflow platform, marketplace, dashboard, or general-purpose AI wrapper. The goal is a narrow trust boundary with verified-result-or-safe-failure behavior.

---

## What This Repo Does Not Represent

This repo should **not** be interpreted as:

- the current primary public evaluation kit
- a broad gateway-first public product
- a broad public API catalog
- a marketplace
- a multi-workflow public platform
- the complete private implementation repo with all internal operational detail

---

## Contact

For current Phase 1 evaluation questions or payload discussion:

- [tetsutetsu11@icloud.com](mailto:tetsutetsu11@icloud.com)

For the current public evaluation materials, use:

- **[dlx-public-kit](https://github.com/kodomonocch1/dlx-public-kit)**

---

## Current Role of This Repository

Use this repository only as one of the following:

- historical / transitional public context
- kernel-oriented naming/context companion
- a pointer toward the current public evaluation repo

The active public evaluator path for Phase 1 has moved to:

- **[dlx-public-kit](https://github.com/kodomonocch1/dlx-public-kit)**
