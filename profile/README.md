# OpenDPP

**Digital Product Passports for the EU — built standards-first.**

OpenDPP is a B2B Digital Product Passport service for the EU Ecodesign for Sustainable Products
Regulation (ESPR) and the Battery Regulation. Every public passport URL serves
**standards-conformant, independently verifiable** output under HTTP content negotiation — so a
passport is consumable by IDTA AAS tooling and W3C Verifiable Credential verifiers alike, not just by
us.

### Two interoperability doors

- **AAS / IDTA** — `application/aas+json` + AASX, conformant to IDTA-01001-3-1 (AAS v3.0).
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

### What we publish vs. keep private

The **interoperability contract is open** (this org). The **product backend** — tenancy, key custody,
billing, the SSR/portal application — stays private. You never need the backend to consume or conform
to OpenDPP output.

---

<sub>OpenDPP is an ESPR-readiness / interoperability node: it produces validator-conformant,
independently verifiable output. Regulatory compliance is a determination for the operator and the
competent authority.</sub>
