# @paperclipai/adapter-bob-shell

External Paperclip adapter for **IBM Bob Shell** (`bob run`) — runs IBM Bob in
non-interactive mode as a managed AI agent inside a Paperclip company.

## Installation

In the Paperclip Board, go to **Adapter Manager → Install Adapter** and enter:

```
@paperclipai/adapter-bob-shell
```

Or install via local path during development (see below).

## Prerequisites

- IBM Bob Shell CLI installed (`bob` on PATH)
- IBM account with Bob Shell access
- License accepted: `bob --accept-license`

## Local development

```bash
npm install
npm run build
```

Then in Paperclip Board: **Adapter Manager → Install Adapter → Local path** → point at this directory.

## External adapter API

This package exports `createServerAdapter()` from its root, which is the
entrypoint Paperclip uses to load external adapters.

```ts
import { createServerAdapter } from "@paperclipai/adapter-bob-shell";
const adapter = createServerAdapter();
// adapter.type === "bob_shell"
```

## License

MIT
