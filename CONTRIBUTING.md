# Contribute

This site is a personal documentation portfolio, but typo fixes, broken-link reports, and small clarifications are welcome.

## How to contribute

### Option 1: Edit directly on GitHub

1. Navigate to the page you want to edit.
2. Click the pencil icon (Edit this file).
3. Make your changes and open a pull request.

### Option 2: Local development

1. Fork and clone this repository.
2. From the repo root: `nix develop` (or install Node 20 + `npm i -g mint` manually).
3. Run `mint dev` to preview at <http://localhost:3000>.
4. Make your changes on a feature branch.
5. Run `mint broken-links` to validate.
6. Commit and open a pull request.

## Writing guidelines

- Active voice, second person ("you")
- One idea per sentence
- Sentence case for headings
- Code formatting for file names, commands, paths, and code references
- Diagrams over prose where structure matters

## Content boundaries

This site documents public repositories in depth. A private repository may be
named in an index or "related repos" list — bare name, no link, labeled
`(private)` — when its existence is needed for the map to make sense. Do not
add:

- A link to a private repository (it 404s or redirects for every visitor)
- Any description of a private repository's contents, internals, or topology
- Real internal IP addresses or hostnames
- Credentials, tokens, or other sensitive data

When in doubt, ask in an issue before opening a PR.
