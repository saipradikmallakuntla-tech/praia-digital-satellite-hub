# Coastal Satellite Network — seven direct GitHub Pages sites

Architecture revision: 2026-11-15. This document describes the implementation; observed build, HTTP and functional results belong in [DIRECT_PAGES_NETWORK_RELEASE.md](DIRECT_PAGES_NETWORK_RELEASE.md). The earlier four-site verification remains available in Git history and must not be mistaken for the seven-site release.

## Topology and scope

One owned hub plus six owned satellites under `saipradikmallakuntla-tech`, all independent static project sites. Each page provides six ordinary `a[data-network]` links to all other sites: 42 unique directed edges, excluding self-links. Navigation remains usable with JavaScript disabled, independent of hub filters or app state. Full URLs are listed in [NETWORK.md](NETWORK.md).

Only these seven repositories may be modified. `praia-digital-seo-audit` is an excluded fork; its files, branches and disabled Pages setting remain untouched. No upstream or third-party repository changes, pull requests, custom-domain settings or CNAME files are part of this release. Existing contextual links to Praia Digital remain external, with no affiliation or reciprocal integration assumed.

## Responsibilities

| Repository | Responsibility and limits |
| --- | --- |
| praia-digital-satellite-hub | PT/EN directory, six categories, municipality filters, strict six-app URL allowlist and release documentation. Coverage means references/examples, not availability. |
| maresia-em-dia | Original PT maintenance organiser, recurrence, ICS/JSON export and local records. Not an engineering inspection or a prescribed maintenance schedule. Navigation-only HTML change in this release. |
| acesso-a-praia | Original PT documentary beach-access pilot with dated sources and unknowns. No current operation or accessibility guarantee. Navigation-only HTML change. |
| costa-em-contexto | Original PT regional source/scale guide. No parcel-level safety decision or real-time hazard alert. Navigation-only HTML change. |
| rota-ciclo-costeira | New PT/EN bounded distance/speed/breaks calculator with optional return and preparation checklist. No route planning, field-verified cycleway, weather or safety prediction. |
| balneabilidade-guia | New PT/EN UTC date comparator, evidence filters and checklist. Four fictional exercises; no actual bulletin, validity threshold or bathing clearance. CETESB is linked as an official starting point. |
| feiras-e-servicos-litoral | New PT/EN four-record fictional directory, city/day/category/search filters and BRL budget calculator. No verified venue, schedule, price or operation. Municipal portals are starting points only. |

## Publication and files

Each site is published from `main` and `/` using branch-based Pages (`legacy`), with `.nojekyll`, enforced HTTPS and a self-referencing canonical `https://saipradikmallakuntla-tech.github.io/<repo>/`. No DNS or custom-domain dependency. All runtime CSS and JavaScript are local; no npm/Vite build or remote runtime library is needed.

New repositories contain `index.html`, `styles.css`, `site.js`, `core.js`, `app.js`, `.nojekyll`, `README.md` and `NETWORK.md`. Pure core functions also export through CommonJS for Node tests. Static content uses Portuguese defaults; `site.js` applies English through explicit text attributes and a `coastal:language` event. Dynamic errors/results/filter cards are translated by each app. User input is rendered with textContent, not executable HTML. Invalid query options fall back to allowed defaults. Language can be selected with `?lang=en`; hub card links preserve language only for bilingual apps. Fixed footer network links always point to exact canonical roots.

## Data boundaries and safety

New apps do not send/store form data, request geolocation, track visitors, fetch live APIs or require accounts. Original browser-local records and datasets are unchanged. All project paths share one origin: localStorage is not a security isolation boundary. No sensitive app records are added to shared URLs or committed to repositories. Sample names, dates and day-of-week values are explicitly fictional; an editorial link-selection date is not an observation, sampling or current-service verification date.

## Verification contract

Check HTML structure/labels/unique IDs/local assets/canonicals; JavaScript syntax; pure calculator and filter boundaries; browser form interaction and error focus; PT/EN dynamic state; keyboard navigation; responsive overflow; original-app regression flows; all 42 HTML edges with JavaScript off. After asynchronous builds, require TLS-verified HTTPS 200 at all seven exact canonical roots, compare deployed HTML and runtime assets with committed bytes, and re-read Pages settings. Record tests and limitations honestly in the release report; availability is a timestamped snapshot, not an uptime or real-world safety guarantee.
