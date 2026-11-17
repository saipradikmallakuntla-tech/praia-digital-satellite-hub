# Coastal Satellite Hub / Central de Aplicativos do Litoral

[Open the direct HTTPS hub](https://saipradikmallakuntla-tech.github.io/praia-digital-satellite-hub/)

PT/EN directory of six independent coastal utilities. Six category filters, municipality filters, safe allowlisted app links, zero-match/reset states and ordinary HTML navigation to every satellite. Filters describe documentary coverage or fictional examples, not operational availability. Three original apps keep their Portuguese interfaces and existing logic; the new three apps and hub support PT/EN.

Static local HTML/CSS/JS, no build, dependency, analytics, backend, custom domain or CNAME file. Serve with `python3 -m http.server 8080`. GitHub Pages: `main` root, `.nojekyll`, HTTPS enforced. `?lang=en` selects English. Network links work without JavaScript.

- [Architecture](SATELLITE_NETWORK_ARCHITECTURE.md)
- [Network URL policy](NETWORK.md)
- [Release evidence and test limitations](DIRECT_PAGES_NETWORK_RELEASE.md)

New utility datasets are explicitly fictional/reference-only. No current water-quality, verified cycling route or real market/service schedule is asserted. External links are contextual references, not an affiliation or an upstream integration.

## Cross-app asset sync and editorial review

[Cross-App Asset Sync and Trigger Workflow](DATA_ASSET_SYNC_AND_TRIGGER_WORKFLOW.md) documents the human-gated Gmail → private Drive register → GitHub Markdown → Gmail draft checklist. Documentation only: no automatic application-data sync, email sending, code changes, merge or deployment. Existing development commands above are historical context, not steps in this workflow.
