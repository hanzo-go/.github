# LLM.md — hanzo-go

Machine-oriented guide for AI agents and coding assistants working in this org.

## What this org is

`hanzo-go` is the **per-language org for Go** in the Hanzo ecosystem. It holds
real, idiomatic Go code (not docs stubs). Hanzo is the **Open AI Cloud** — a full
AI SDK / AI cloud, not a proxy.

## Canonical SDK model (two lines, every language)

1. **Full Cloud SDK** — generated from the cloud OpenAPI, covers all of `/v1`.
   Real code lives in the per-language org: **`hanzo-go/sdk`** (this org).
   A thin docs/landing wrapper lives at `hanzoai/go-sdk`; meta index `hanzoai/sdk`.
2. **AI / Agents SDK** — hand-crafted flagship (models, agents, tools, memory,
   MCP, inference). Python `hanzo` (`hanzoai/python-sdk`) is most complete;
   Node `@hanzo/ai` (`hanzo-js/ai`). In Go, these helpers ship in `hanzo-go/sdk`.

## Where real code lives

- Full Go Cloud SDK → **`hanzo-go/sdk`**
- Install: `go get github.com/hanzo-go/sdk`

## Brand rules (never violate)

- **Never** call Hanzo an "LLM gateway" and never position it against LiteLLM.
  It is a full AI SDK / AI cloud.
- API paths are **`/v1/`** only — never an `/api/` prefix.
- **Zen** models are our own family — never name upstream models.
- Positioning: "Hanzo — the Open AI Cloud. Open source. Every language. On-chain settlement."

## Reference

Canonical architecture: `~/work/hanzo/SDK-ARCHITECTURE.md`.
