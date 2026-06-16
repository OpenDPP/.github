# Contributing to OpenDPP

Thanks for your interest. OpenDPP's **public** repositories (this org) are the open interoperability
boundary of a B2B Digital Product Passport service whose product backend is **private**. That shapes
how to contribute.

## What lives where

- **[`opendpp-interop`](https://github.com/OpenDPP/opendpp-interop)** — the interop kit: the official
  schemas, live-reproducible samples, the conformance validator, the public OpenAPI contract, and the
  AAS + UNTP field mappings. The **source of truth is the OpenDPP product** (private); the artifacts
  here are published outputs of it.

## How to contribute

- **Conformance gaps** — a place where OpenDPP's AAS or UNTP/VC output doesn't match the standard.
  Open a *Conformance gap* issue with the URL + `Accept` header you used and the expected vs actual.
  These are the most valuable reports: they're fixed upstream in the product, then re-published here.
- **Kit fixes** — a validator bug, a doc error, a stale sample, a schema-copy refresh. PRs welcome.
- **Please don't** send PRs that try to change product behaviour — that code isn't in these repos.

## Ground rules

- Keep PRs focused; explain what & why; link the issue.
- Samples must stay faithful, reproducible outputs of the live service (CI re-validates them).
- Never commit secrets or private keys — CI runs a secret scan.
- Be respectful — see [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).
