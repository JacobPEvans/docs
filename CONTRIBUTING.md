# Contribute

This repository is the generated public projection of the private documentation
site. Direct content contributions are not accepted here.

## How to contribute

Documentation changes must be authored in `dryvist/docs-starlight`. The
publisher selects the public-safe projection, converts it to Mintlify, scans
it, and opens the public pull request. A human reviews every generated pull
request before merge.

Pull requests to this repository are limited to publisher and repository
control-plane maintenance. Do not edit pages, generated assets, or `docs.json`
by hand.

## Content boundaries

This site documents public repositories in depth. A private repository may be
named in an index or "related repos" list — bare name, no link, labeled
`(private)` — when its existence is needed for the map to make sense. Do not
add:

- A link to a private repository (it 404s or redirects for every visitor)
- Any description of a private repository's contents, internals, or topology
- Real internal IP addresses or hostnames
- Credentials, tokens, or other sensitive data

The publisher fails closed when a page cannot be proven public-safe.
