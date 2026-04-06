# Aethelred Sovereign Copilot

Aethelred Sovereign Copilot is the official VS Code extension for working with the Aethelred protocol, validator tooling, and sovereign compute workflows.

It adds editor-side diagnostics, hover intelligence, code lens actions, Helix language support, and direct CLI-backed protocol checks for developers building on Aethelred.

## Core capabilities

- Real-time compliance and sovereignty diagnostics for supported source files
- Hover details for sovereign functions, hardware targets, and policy context
- Code lens actions for scans, remediation, and protocol-aware quick actions
- Status bar visibility for jurisdiction, CLI availability, and active checks
- Helix DSL syntax highlighting and snippets for protocol-native workflows
- Direct integration with the `aethel` CLI for local and network-aware checks

## Supported languages

- Python
- Rust
- TypeScript
- JavaScript
- Helix DSL (`.helix`, `.hlx`)

## Requirements

The extension is designed to work with the Aethelred CLI.

Recommended installation paths:

```bash
cargo install aethelred-cli
```

Or use the CLI installation instructions from the protocol docs:

- [Aethelred CLI installation](https://docs.aethelred.io/cli/install)

## Configuration highlights

| Setting | Default | Purpose |
| --- | --- | --- |
| `aethelred.jurisdiction` | `Global` | Active jurisdiction for diagnostics |
| `aethelred.compliance.regulations` | `[`"`GDPR`"`]` | Ruleset used during checks |
| `aethelred.linting.enabled` | `true` | Enables background diagnostics |
| `aethelred.linting.onSave` | `true` | Runs checks on save |
| `aethelred.hardware.target` | `auto` | Preferred hardware profile |
| `aethelred.network.chain` | `testnet` | Active network profile |
| `aethelred.network.endpoint` | `https://api.testnet.aethelred.io` | Protocol API endpoint |

## Install from source

```bash
npm install
npm run build
```

To package a VSIX locally:

```bash
npm run package:check
```

The packaged extension is written to `dist/aethelred-sovereign-copilot.vsix`.

## Development

```bash
npm install
npm run build
npm run lint
```

In VS Code:

1. Open this repository.
2. Run `Extensions: Show Running Extensions` if you need to inspect activation state.
3. Launch the extension host with `F5`.

## Repository layout

- `src/` — extension source
- `syntaxes/` — Helix grammar and language configuration
- `snippets/` — language snippets
- `assets/` — icons and package assets

## Security

Security reports should not be filed in public issues.

Use:

- `security@aethelred.io`
- [Security policy](SECURITY.md)

## License

Apache-2.0
