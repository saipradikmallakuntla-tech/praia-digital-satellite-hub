# Praia Digital Satellite Network — Architecture and Final Verification

## 1. Verification snapshot

**Live HTTP checks completed: 2026-11-14 at 19:31:34 UTC.** GitHub Pages settings were inspected during the same verification pass. All four public sites returned **HTTP 200 over HTTPS**, using normal TLS certificate and hostname validation. Requests starting with HTTP also resolved to the corresponding HTTPS URL and returned 200.

| Repository | Canonical live URL | HTTPS GET | TLS validation | Pages status | HTTPS enforced | Publish source |
| --- | --- | --- | --- | --- | --- | --- |
| [maresia-em-dia](https://github.com/saipradikmallakuntla-tech/maresia-em-dia) | [Maresia em Dia](https://saipradikmallakuntla-tech.github.io/maresia-em-dia/) | 200 | Passed | built | true | main / |
| [acesso-a-praia](https://github.com/saipradikmallakuntla-tech/acesso-a-praia) | [Acesso à Praia](https://saipradikmallakuntla-tech.github.io/acesso-a-praia/) | 200 | Passed | built | true | main / |
| [costa-em-contexto](https://github.com/saipradikmallakuntla-tech/costa-em-contexto) | [Costa em Contexto](https://saipradikmallakuntla-tech.github.io/costa-em-contexto/) | 200 | Passed | built | true | main / |
| [praia-digital-satellite-hub](https://github.com/saipradikmallakuntla-tech/praia-digital-satellite-hub) | [Central de Aplicativos do Litoral](https://saipradikmallakuntla-tech.github.io/praia-digital-satellite-hub/) | 200 | Passed | built | true | main / |

Additional checks passed:

- Each live page has a self-referencing canonical URL matching the HTTPS URL above, including its trailing slash.
- All three satellites contain direct HTTPS links back to the hub in their published HTML.
- The hub contains direct HTTPS links to all three satellites. Every satellite also links to the other two.
- All four GitHub Pages sites are public, use branch publishing (`build_type: legacy`) from `main` and `/`, and have no custom domain configured.
- Every repository contains `.nojekyll` at its publication root.
- The live HTML bytes match the corresponding repository `index.html` Git blob, confirming that the verified pages are the inspected application pages rather than generic GitHub error pages.

### Published HTML identity

These are Git **blob** SHAs for the verified `index.html` content, not commit SHAs:

| Application | HTML bytes | Git blob SHA |
| --- | ---: | --- |
| Maresia em Dia | 6297 | `defaf12f84a74e0f3df43712c1dcd4ea126c44ab` |
| Acesso à Praia | 6813 | `c4312c89f7116aab49443a458788039fe50d02af` |
| Costa em Contexto | 8248 | `e9342fe20c65ad96dd6d90add9692b733edd058d` |
| Satellite Hub | 9045 | `05b243169d548b8651e7767efa8d48a090aa0cd4` |

The hub branch head inspected before this documentation-only change was `97b6ad6d3a924610140c72a0b0dc6cfba65f39f0`. Adding this document can trigger another Pages build; the snapshot above records the actual observed deployment, not an assumption about a future build.

## 2. Application responsibilities

- **Maresia em Dia:** component maintenance planning, recurring due dates, local records, calendar export, backup and printable output. It organizes care; it is not an engineering inspection or a source of prescribed maintenance intervals.
- **Acesso à Praia:** entrance/service references filtered by city and needs, with dated source evidence, unknowns and service status. A documented reference does not guarantee present-day operation or suitability for every visitor.
- **Costa em Contexto:** a regional flood/landslide susceptibility source-and-scale guide. It helps users interpret map provenance and limitations; it does not produce parcel-level safety clearance or real-time hazard warnings.
- **Satellite Hub:** the central directory, with promotional cards, descriptions, city/category filters and links to the three independent tools.

## 3. Interlinking map

```text
                      praia-digital-satellite-hub
                       /           |           \
                      v            v            v
              maresia-em-dia  acesso-a-praia  costa-em-contexto
                      ^            ^            ^
                      |            |            |
                      +---- each links back ----+

All three satellites also link directly to one another.
Hub and satellites -> contextual resources on https://praia.digital/
```

Observed contextual routes:

| Origin | Contextual Praia Digital destinations |
| --- | --- |
| Maresia em Dia | [Owner central](https://praia.digital/meu-imovel.html), [inspection checklist](https://praia.digital/apps/checklist-vistoria/) |
| Acesso à Praia | [Neighborhood index](https://praia.digital/bairros/index.html) |
| Costa em Contexto | [Guarujá city guide](https://praia.digital/cidades/guaruja.html), [property report](https://praia.digital/apps/relatorio-imovel/) |
| Satellite Hub | [Main platform](https://praia.digital/), [existing app network](https://praia.digital/apps/), [neighborhood index](https://praia.digital/bairros/index.html) |

The Praia Digital platform remains an external destination. These links do not imply official affiliation, reciprocal upstream links, shared accounts, or access to a live Praia Digital API. No upstream change is claimed by this verification.

## 4. Static architecture and URL policy

- Four independently published GitHub Pages project sites under `saipradikmallakuntla-tech`.
- Static `index.html`, local CSS and plain JavaScript; no npm/Vite compilation is needed for branch-root publication.
- Local `core.js` files separate domain logic where present; Acesso à Praia loads a local `data.js` reference dataset.
- HTML provides semantic page structure, descriptions, Open Graph metadata and WebApplication JSON-LD. The directory links remain ordinary anchors rather than depending on a router.
- Canonicals identify each application's own HTTPS root. The hub is a directory, not the canonical replacement for its satellites.
- Cross-repository navigation uses full HTTPS project URLs, avoiding relative-path mistakes between Pages project folders.
- App records and exports must not be committed as user data or added to share URLs. Browser-local storage is not an independent security boundary between these project paths because they share the same origin.

## 5. Evidence and verification method

1. Read each repository's GitHub Pages configuration; check `html_url`, `status`, `https_enforced`, `public` and `source`.
2. GET each canonical HTTPS URL with certificate verification enabled; require status 200 and the expected final URL.
3. Request the HTTP variant and confirm the final response is the corresponding HTTPS page.
4. Read live canonical tags and network anchors; compare the live HTML's Git blob hash against the repository's `index.html` blob SHA.
5. Confirm `.nojekyll` in every repository and inspect the hub's existing root before adding this document.

Public endpoint checks can be repeated without credentials:

```sh
for repo in maresia-em-dia acesso-a-praia costa-em-contexto praia-digital-satellite-hub; do
  curl --fail --silent --show-error --location --proto '=https' \
    --output /dev/null --write-out '%{http_code} %{url_effective}\n' \
    "https://saipradikmallakuntla-tech.github.io/$repo/"
done
```

The HTTP checks are an availability snapshot, not a continuous uptime guarantee. This pass verifies deployment, TLS, published HTML identity, canonical URLs and network links. It does not certify real-world accessibility, environmental safety or every interactive behavior in every browser. Source dates and operational service status still need ongoing editorial review.

## 6. Next-batch ideas — exploratory, not launched

Before creating further repositories, audit the current Praia Digital/ASF tools again for overlap and establish authoritative data sources.

- **Actual-use utility diary:** local water/energy meter readings and consumption differences for intermittently occupied coastal homes; actual observations rather than investment forecasts.
- **Dated rules-of-use evidence board:** organize source documents, responsible contacts and unresolved questions about condominium/municipal visitor and hosting rules, without issuing legal conclusions.
- **Coastal waste and disposal reference:** verified, dated municipal guidance for recycling, bulky-item collection and appropriate disposal, with location coverage and unknowns explicit.

These ideas are a backlog for discovery, not an authorization to create additional repositories or a claim that their data is already verified.
