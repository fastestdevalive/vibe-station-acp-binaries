# vibe-station-acp-binaries

Prebuilt [ACP](https://agentclientprotocol.com) adapter binaries used by [vibe-station](https://github.com/fastestdevalive/vibe-station):

| Binary | Mirrors upstream | Port revision |
|---|---|---|
| `claude-acp` | `@agentclientprotocol/claude-agent-acp` 0.94.0 | `ffb031946e769d68eb47bed355f5d66a63c2127a` |
| `codex-acp` | `@agentclientprotocol/codex-acp` 2.2.2 | `b7391e216a7eabdd89bdcad22cacbbaf06f28c72` |

Targets: `aarch64-apple-darwin`, `x86_64-unknown-linux-{gnu,musl}`, `aarch64-unknown-linux-{gnu,musl}`.
Each release has one `<name>-acp-<target>.tar.gz` per target and a `SHA256SUMS` file. vibe-station pins the version and
SHA-256 per target and verifies them on download; verify `SHA256SUMS` yourself before running anything else from here.

Notes: the musl builds are fully static; the claude `gnu` builds link OpenSSL 3 dynamically (`libssl.so.3`).

These binaries are provided for use with vibe-station. See `NOTICE` for upstream attribution.
