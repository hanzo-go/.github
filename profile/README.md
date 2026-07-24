# Hanzo for Go

**Hanzo — the Open AI Cloud. Open source. Every language. On-chain settlement.**

This is the Go home of Hanzo. Real, idiomatic Go code lives here — the full
Cloud SDK you build against, plus the AI/agents library. We ship Hanzo in Go
because we genuinely build in Go.

## What's here

- **[`hanzo-go/sdk`](https://github.com/hanzo-go/sdk)** — the **full Hanzo Cloud SDK for Go**.
  Generated from the cloud OpenAPI, it covers the entire `/v1` surface: AI
  (models, agents, inference, embeddings), compute, data, network, security
  (IAM, KMS), platform, observability, web3, and apps. One typed client for
  every Hanzo service.
- The same package carries the **AI / agents** helpers — Zen models (our own
  model family), agents, tools, memory, and MCP — for building AI-native Go
  programs.

## Install

```sh
go get github.com/hanzo-go/sdk
```

## Usage

```go
package main

import (
	"context"
	"fmt"

	hanzo "github.com/hanzo-go/sdk"
)

func main() {
	client := hanzo.NewClient() // reads HANZO_API_KEY
	models, err := client.Models.List(context.Background())
	if err != nil {
		panic(err)
	}
	fmt.Println(models)
}
```

## Repositories

| Repo | What it is |
|------|------------|
| [`sdk`](https://github.com/hanzo-go/sdk) | Full Hanzo Cloud SDK for Go — all of `/v1`, plus AI/agents. `go get github.com/hanzo-go/sdk` |

## Also available in

Every language gets its own home for real code:

- [`hanzo-js`](https://github.com/hanzo-js) · JavaScript / TypeScript
- [`hanzo-py`](https://github.com/hanzo-py) · Python
- [`hanzo-rs`](https://github.com/hanzo-rs) · Rust
- [`hanzo-cpp`](https://github.com/hanzo-cpp) · C++
- [`hanzo-swift`](https://github.com/hanzo-swift) · Swift
- [`hanzo-kt`](https://github.com/hanzo-kt) · Kotlin

Umbrella org: **[`hanzoai`](https://github.com/hanzoai)** — every product and SDK
in one place. Go docs/landing wrapper: **[`hanzoai/go-sdk`](https://github.com/hanzoai/go-sdk)**.
Meta index: **[`hanzoai/sdk`](https://github.com/hanzoai/sdk)**.

---

[hanzo.ai](https://hanzo.ai) · [docs](https://docs.hanzo.ai) · The Open AI Cloud.
