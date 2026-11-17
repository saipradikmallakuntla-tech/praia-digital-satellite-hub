# Praia Digital — Cross-App Asset Sync and Trigger Workflow

[Back to the hub README](README.md)

Documentation edition: 17 November 2026 UTC. Status: process documentation published for team review; substantive editorial decisions remain unapproved unless a named human reviewer explicitly records approval.

## 1. Purpose and hard boundaries

This is a 100% non-coding, human-initiated workflow for synchronizing editorial metadata, review evidence and document links across Gmail, Google Drive and GitHub. It is not synchronization of browser-local app records, a live-data feed, an automatic publication pipeline or an integration with the Praia Digital production site.

The authorized repository write scope for this edition is exactly two paths in `saipradikmallakuntla-tech/praia-digital-satellite-hub` on `docs/asset-sync-workflow`: this guide and the reciprocal cross-reference in `README.md`. The branch starts from reviewed `main` commit `0cd9842627f0de5328af2dd82a4d02a227b3f5b2`. Leave `main`, existing documentation branches and all three satellite repositories unchanged.

Never edit HTML, CSS, JavaScript, `sw.js`, application datasets, settings or workflows. Never execute repository programs, test suites, browser tests, test scripts or byte-hash scripts. Do not create PRs, merge, deploy, change Pages settings, add webhooks or install scheduled automation. Do not read or write upstream repositories for this workflow; in particular, no writes to `acarolmourad-commits`. No changes to the separately linked audit repository are authorized.

Gmail operations are read-only discovery and creation of a new, standalone draft only. Never send, forward, reply-send, auto-address or automatically distribute external email. Never modify or delete an existing draft. A draft is not an approval, notification delivery or publication receipt.

## 2. Network scope and editorial limits

The full network remains seven independent sites: one hub and six utilities. This workflow reviews only the hub and the following three original satellites; it does not remove the other three utilities or redefine them as production-site children. See [network policy](NETWORK.md) and [architecture](SATELLITE_NETWORK_ARCHITECTURE.md) for existing descriptive context, not authorization to run their historical technical verification instructions.

| Property | Editorial responsibility | Limits to preserve |
| --- | --- | --- |
| Hub | PT/EN directory and context selection; common documented return label is “Central de apps”. | Category/municipality filters describe documentary coverage or examples, not operational availability. No self-return or institutional affiliation is implied. |
| Maresia em Dia | Portuguese maintenance organization and local records. | Not an inspection, prescribed schedule or professional advice. ICS is a three-occurrence-per-component snapshot, not automatic synchronization. Do not import browser-local records into this workflow. |
| Acesso à Praia | Portuguese documentary references for five entries/service poles in Santos and Praia Grande. | No field inspection or current operation confirmed. Unknown never means yes. Source dates remain 20 July 2026 for Santos and 30 December 2025 for the Praia Grande announcement; a later review does not renew them. No accessibility, operating-hours or bathing-safety guarantee. |
| Costa em Contexto | Portuguese source and scale literacy for the Guarujá documentary pilot. | Preserve SGB/IPT 2015 and 1:25,000 scale. Regional susceptibility is not parcel-level risk, property certification or a current hazard alert. Other cities remain unreviewed. |

Only the hub is PT/EN within this four-property scope. Preserve original Portuguese app identities, geographic limits, source dates and unknowns. Existing shared-origin browser storage is not a security isolation boundary; do not collect personal app records or place sensitive information in URLs.

## 3. Sources of truth and privacy

| App/artifact | Authoritative for | Not authoritative for |
| --- | --- | --- |
| Gmail communication | What a correspondent actually supplied or requested, with original thread/date. | Substantive approval unless an authorized named reviewer explicitly grants it; source truth or current service operation merely because mail arrived. |
| Private Drive register | Review evidence, original source/revision/review dates, ownership, permissions, decisions and synchronization receipts. | Public release evidence, automatic verification of facts or permission to expose private material. |
| GitHub Markdown | Versioned, sanitized process guidance and documentation proposals at a specific branch/commit. | Live application behavior, production rollout, inherited approval or automatic data synchronization. |
| Gmail draft | A reviewable checklist and pointers awaiting deliberate human handling. | A sent message, approved wording or completed team notification. |

The private register is titled **Praia Digital — Cross-App Asset Sync & Editorial Register**. Create it in the owner's My Drive without granting anyone, domain or public-link access. Verify actual permissions before recording it as private. Do not broaden access or send invitations.

These repositories are public. Keep message bodies, personal addresses, attachment contents, private Drive URLs/file IDs, Gmail thread/draft IDs and other restricted evidence out of GitHub. The private register may link outward to public GitHub documents. This public guide intentionally identifies the private register by title only. Minimize retained information and record provenance, access restrictions and any reuse/rights uncertainty before considering an asset publishable.

## 4. Trigger catalog — proposed, not installed automation

Every trigger below requires a person to initiate review. No Gmail filter/forwarder, Drive watcher, GitHub Action, webhook, scheduler or cross-app agent runs automatically.

| Trigger | Human triage | Drive artifact/decision | Permitted next step |
| --- | --- | --- | --- |
| New relevant communication or asset reference | Confirm relevance, source, date, consent/reuse limits and affected property. | New trigger record linked to an asset record; retain only necessary private evidence. | Propose sanitized Markdown documentation only after review. |
| Correction, conflicting evidence or safety-sensitive claim | Preserve both accounts and distinguish unknown, disputed and confirmed. | Conflict record with source dates and a qualified reviewer where needed. | Hold unsupported wording; prepare a recipient-free review draft. |
| Existing Drive asset revised | Check stable file ID and native revision/modified metadata; do not overwrite history. | Revision entry with original source date, review date and superseded record link. | Reopen human review; do not propagate “approved” automatically. |
| Markdown changed on an owned documentation branch | Read the exact file and native GitHub comparison; confirm allowed paths. | Branch/commit/file links and decision reference. | Update the private receipt; no merge or deployment. |
| Review due, evidence stale or owner missing | A person checks next-review dates and outstanding actions. | Owner/reviewer unassigned or evidence-stale flag. | Request a named reviewer through a saved draft; no invented assignment. |

These are workflow examples, not claims that incoming mail, new assets or external events were observed.

## 5. Private register structure

Use stable human-readable IDs; no byte hashes are required. Maintain four sections:

1. **Asset register** — asset ID; title/type; affected property; stable Drive file ID/link or source pointer; original source/publication date; native modified/revision date; review date; evidence limitations; reuse/access restrictions; owner/reviewer; status; next action; related trigger/decision IDs; exact GitHub path, branch and immutable commit link; draft reference when one exists.
2. **Communication/trigger log** — trigger ID/type; observed versus proposed; actual source/thread link when available; received date; discovery/review date; affected asset/property; deduplication key; required action and current status. If no communication is found, record the search scope/result instead of inventing a correspondent, message or thread.
3. **Editorial decisions and approvals** — decision ID; question; supporting/conflicting evidence; proposed wording; named decision owner and qualified reviewer when required; approval scope, explicit outcome and date; conditions; next review. “Unassigned”, “unknown” and “not approved” are valid states.
4. **Synchronization receipts and outstanding actions** — manual authorization and scope; baseline references; created artifact IDs/links; native read-back/comparison results; unchanged-branch/draft checks; unresolved gaps; next responsible person/action. Record only observed success, not an intended outcome.

Suggested record states: Logged → Evidence pending → Human review pending → Approved for documentation → Documented → Draft ready. A person records each transition; none is automatic. Documentation publication approval does not approve substantive editorial claims or technical implementation. Until a reviewer is named and approval is recorded, substantive proposals remain pending.

Keep original source date, asset modified date, review date and documentation publication date separate. A new review timestamp does not make an old source current. Deduplicate by existing trigger/thread, stable asset ID, affected GitHub path and issue/revision; append a revision/history entry instead of cloning records. Check for an existing branch, register and draft before retrying a partially completed run.

## 6. Manual operating checklist

1. **Authorize and scope.** Obtain explicit human authorization for repository publication or other consequential changes. Record the two-path allowlist, target branch and reviewed base. Recheck existing state; stop on an unexpected branch collision or concurrent edit. Never force-update another person's work.
2. **Discover read-only.** Search relevant Gmail terms and existing drafts, inspect relevant Drive documents and read current Markdown/branches in the four owned repositories. Exhaust returned pagination. Keep drafts separate from received communications and do not change mail labels/read state or existing artifacts.
3. **Register private evidence.** Create or update the relevant private register record. Link existing evidence rather than mirroring private content into public repositories. Classify provenance, source date, review date, access restrictions, uncertainty and affected property.
4. **Obtain appropriate review.** Assign a named editorial owner through a human decision, not inference. Use qualified reviewers for maintenance, accessibility or regional-risk claims. Missing approval blocks substantive claims; it does not transform a clearly labeled process template into an approved editorial decision.
5. **Publish the allowed documentation proposal.** For this edition, add this guide and append only its relative README cross-reference on `docs/asset-sync-workflow`, with a reciprocal README link here. Keep existing documentation branches separate; do not merge their proposals or inherit approval. Leave the three satellite repositories read-only.
6. **Verify using native read-only APIs.** Read back both Markdown files at the resulting commit and inspect GitHub's comparison against the reviewed base. Require exactly this guide added and `README.md` modified. Confirm the original twelve branch heads, including all four `main` heads, are unchanged. This is document read-back, not execution of code, a test suite, a byte-hash script, a deployment check or an accessibility certification.
7. **Prepare correspondence only.** Create one new standalone Gmail draft with subject `[TEAM REVIEW ONLY] Praia Digital — Cross-App Sync Checklist`. Use a genuine `text/plain` body, not HTML or an HTML alternative. Leave To, Cc and Bcc blank; add no attachments, signature, inherited recipients or reply-thread context. Include the checklist, document links and outstanding decisions. Do not invoke any send action.
8. **Close the manual receipt.** Read the new draft back and verify the subject, plain-text MIME type, empty recipients and Drafts-only state. Re-list existing drafts and confirm every pre-existing draft is unchanged. Record the new artifact links/IDs, what was actually checked and what remains pending in the private register. A human may review the draft later; sending is outside this workflow.

## 7. Verified baseline and unresolved evidence

The read-only discovery on 17 November 2026 UTC found no matching Gmail communications in the recent 90-day search or broader date-unrestricted coastal/Praia keyword search. All 36 pre-existing drafts were inspected; none matched this network. Do not fabricate incoming-message triggers or substantive approvals from those empty results.

One matching Drive brief was found: **Praia Digital — IA & Editorial Navigation Brief**, modified 16 November 2026. It is an executive index of prior documentation, not production rollout evidence. It reports fourteen unreviewed decisions, zero substantive editorial approvals and unassigned named owners/reviewers. It remains unchanged by this workflow.

All four owned repositories had `main`, `docs/editorial-navigation-and-ia-standards` and `docs/mobile-nav-and-trail-copy-spec`. The hub had `README.md`, `NETWORK.md` and `SATELLITE_NETWORK_ARCHITECTURE.md`; each of the three satellites had `README.md`. Existing editorial/navigation proposals remain on their separate branches. The [hub's existing governance summary](https://github.com/saipradikmallakuntla-tech/praia-digital-satellite-hub/blob/fce39c45220b88d1abf6f97c0cdfbf2e6bb29f49/README.md) is contextual evidence, not an inherited approval.

`DIRECT_PAGES_NETWORK_RELEASE.md` is referenced by existing hub documentation but absent from every inspected hub branch. Request its approved location or an explicit evidence decision. Do not reconstruct a release receipt, silently remove the gap, execute the historical technical instructions or interpret this workflow publication as proof of runtime behavior.

## 8. Stop, recover and accept

Stop on missing/expired permissions, unexpected writes or paths, confidential material proposed for GitHub, conflicting or stale evidence without review, an existing target with unexplained content, a nonempty recipient field, a MIME body other than plain text, or an action that would send mail, touch code, update another branch or affect upstream repositories. Report the limitation and request a human decision.

For partial success, retain the successful artifact IDs, label pending work honestly and resume only the missing approved step after checking current state. Do not duplicate documents/drafts, force-push, delete artifacts, overwrite existing drafts, roll back branches or broaden sharing as a workaround. Destructive cleanup or a changed scope requires separate approval.

Acceptance requires exactly two Markdown changes on the new hub branch, reciprocal relative links, API read-back of both files, an owner-only Drive register with all four sections and direct GitHub links, one new recipient-free plain-text Gmail draft, all 36 original drafts preserved, and all twelve original branch heads unchanged. No email delivery, operational verification, substantive editorial approval or production implementation is asserted by that acceptance.
