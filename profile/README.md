<p align="center">
  <img src="https://raw.githubusercontent.com/OpenDPP/.github/main/profile/assets/opendpp-mark.png" alt="OpenDPP" width="128" height="128">
</p>

<h1 align="center">OpenDPP</h1>

<p align="center"><strong>Digital Product Passports for the EU — built standards-first.</strong></p>

OpenDPP is a B2B Digital Product Passport service for the EU Ecodesign for Sustainable Products
Regulation (ESPR) and the Battery Regulation. Every public passport URL serves
**standards-conformant, independently verifiable** output under HTTP content negotiation — so a
passport is consumable by IDTA AAS tooling and W3C Verifiable Credential verifiers alike, not just by
us.

### Two interoperability doors

- **AAS / IDTA** — `application/aas+json` + AASX, conformant to IDTA-01001-3-1 (AAS v3.0/3.1).
- **UNTP + W3C VC** — enveloping `vc+jwt` (VC-JOSE-COSE) or embedded `vc+ld+json` (W3C Data Integrity,
  `ecdsa-jcs-2019`), conformant to UNTP DigitalProductPassport v0.7.0, with `did:web` issuer keys and
  W3C Bitstring Status List revocation.

### Start here

- 🔗 **Live service:** [opendpp-node.eu](https://opendpp-node.eu)
- 📦 **[opendpp-interop](https://github.com/OpenDPP/opendpp-interop)** — the open interop boundary:
  official schemas, validated samples, a runnable conformance validator, the OpenAPI contract, and the
  field mappings. Everything you need to integrate **without** access to the product source.
- 📖 **API reference:** [opendpp-node.eu/api-reference](https://opendpp-node.eu/api-reference) ·
  machine-readable: [openapi.json](https://opendpp-node.eu/openapi.json)
- 🤖 **[opendpp-knowledge](https://github.com/OpenDPP/opendpp-knowledge)** — the API as a
  machine-readable **OKF (Open Knowledge Format)** bundle for AI agents: cross-linked Markdown concepts
  for every endpoint, schema and webhook, regenerated on each API version. Served live at
  [opendpp-node.eu/okf](https://opendpp-node.eu/okf) and advertised via
  [llms.txt](https://opendpp-node.eu/llms.txt).

### Open client libraries — `@opendpp/*` on npm

Small, Apache-2.0 npm packages that make integrating with the node easier — all provenance-backed:

- 📦 **[`@opendpp/sdk`](https://www.npmjs.com/package/@opendpp/sdk)** — the full typed API client, generated from the OpenAPI contract ([opendpp-sdk](https://github.com/OpenDPP/opendpp-sdk)).
- 📦 **[`@opendpp/gs1`](https://www.npmjs.com/package/@opendpp/gs1)** — GS1 Digital Link builders + mod-10 / GLN check-digit helpers.
- 📦 **[`@opendpp/csv`](https://www.npmjs.com/package/@opendpp/csv)** — CSV → passport mapper to the public ingest shape (bulk import).
- 📦 **[`@opendpp/webhooks`](https://www.npmjs.com/package/@opendpp/webhooks)** — webhook event types + a constant-time HMAC-SHA256 signature verifier.
- 📦 **[`@opendpp/eori`](https://www.npmjs.com/package/@opendpp/eori)** — EORI validation against the EU Commission EOS authoritative service + offline syntax helpers.
- 📦 **[`@opendpp/aeo`](https://www.npmjs.com/package/@opendpp/aeo)** — Authorised Economic Operator (trusted-trader) lookup against the EU Commission EOS service.

```sh
npm install @opendpp/sdk   # or @opendpp/gs1, @opendpp/csv, @opendpp/webhooks, @opendpp/eori, @opendpp/aeo
```

### What we publish vs. keep private

The **interoperability contract is open** (this org). The **product backend** — tenancy, key custody,
billing, the SSR/portal application — stays private. You never need the backend to consume or conform
to OpenDPP output.

---

<sub>OpenDPP is an ESPR-readiness / interoperability node: it produces validator-conformant,
independently verifiable output. Regulatory compliance is a determination for the operator and the
competent authority.</sub>

<sub>© Opendpp UAB · "OpenDPP"™ and the OpenDPP logo are trademarks of Opendpp UAB. The Apache-2.0
license on the open repositories covers the code, not the name or logo — see
<a href="https://github.com/OpenDPP/opendpp-interop/blob/main/TRADEMARK.md">TRADEMARK.md</a>.</sub>
