# docs.jacobpevans.com

[![CI](https://github.com/JacobPEvans/docs/actions/workflows/ci.yml/badge.svg)](https://github.com/JacobPEvans/docs/actions/workflows/ci.yml)

Generated Mintlify projection for
[docs.jacobpevans.com](https://docs.jacobpevans.com). Documentation is authored in
a separate private source; this repository only publishes it.

Built with [Mintlify](https://mintlify.com). The publisher deterministically
converts an approved public projection from Starlight MDX, validates and scans
the result, then opens a generated pull request. Content and `docs.json` must
not be edited directly in this repository.

## Installation

Requires [Nix with flakes](https://nixos.org/) (recommended) or Node 20+
installed manually.

```bash
nix develop      # Dev shell: mermaid-cli + node 20 + jq
npm i -g mint    # First time only: install the Mintlify CLI
```

## Usage

```bash
mint dev           # Preview at http://localhost:3000
mint broken-links  # Validate internal links
```

## Deploy

Push to `main` triggers an auto-deploy via the Mintlify GitHub app. Generated
pull requests require provenance, validation, secret scanning, and a fresh
human approval. Preview branches are a paid Mintlify feature, so the publisher
validates the projection before opening the pull request.

## DNS

`docs.jacobpevans.com` is a CNAME to `cname.mintlify-dns.com`. Mintlify
provisions HTTPS automatically within ~24h of DNS propagation.

## Identity system

Reef Green primary `#4FB3A9`, Coral accent `#E06B4A`, Ink dark bg `#0B1D2A`,
Paper light bg `#F4EFE6`. Geist for display, JetBrains Mono for terminal-style
accents.

## Structure

```text
docs.json                      Mintlify config (theme, palette, fonts, nav)
introduction.mdx               Landing page
how-it-fits-together.mdx       Full portfolio architecture
architecture/                  System overviews, data pipelines, AI dev pipeline
infrastructure/                Terraform module map
configuration/                 Ansible role map
nix/                           Nix ecosystem
ai-development/                Claude, Antigravity, Copilot, MLX
observability/                 Cribl, Splunk, OTEL, MCP
security/                      Doppler, SOPS, Keychain, Bitwarden, BWS, OpenBao
tools/                         Dev utilities
about/                         Bio, homelab tour, reef tank
logo/                          SVG wordmark (light + dark)
favicon.svg                    Favicon
.github/workflows/ci.yml       JSON syntax check + broken-links check
flake.nix                      Reproducible dev shell
```

## Control-plane contributions

See [CONTRIBUTING.md](./CONTRIBUTING.md). Direct documentation edits are not
accepted.

## License

MIT (see `LICENSE`).
