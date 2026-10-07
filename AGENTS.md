---
# AGENTS.md — sheetset-excel-editor (site web)


Static HTML site for the Sheet Set Excel Editor product page.
Deployed via GitHub Pages to https://cad.lessard.xyz/.


## 1. Product facts (canonical — do not change without a DECISION entry)


- Product name: Sheet Set Excel Editor
- Product version: 1.0.0
- Author: Etienne Lessard
- Website: https://cad.lessard.xyz/
- Help: https://cad.lessard.xyz/help.html
- Privacy: https://cad.lessard.xyz/privacy.html
- Support: https://cad.lessard.xyz/support.html
- Support email: support@lessard.xyz
- Public plugin commands: SSEXPORT, SSEIMPORT, SSEABOUT, SSEHELP
  (validation is integrated into SSEIMPORT — there is NO separate
   Validate command and NO SSEVALIDATEXLSX)
- Plugin source repo: D:\Documents\GitHub\SheetSetManager
- Supported AutoCAD products: AutoCAD 2026/2027 and AutoCAD-based
  vertical products 2026/2027


## 2. Stack and conventions


- Pure static HTML. No framework, no build step, no npm.
- CSS inline in each page's <style> block.
- No external dependencies (no CDN, no webfonts, no analytics).
- Each page must remain self-contained.
- Language: English (en).


## 3. Repository structure


    CNAME             ← cad.lessard.xyz
    index.html        ← product page
    help.html         ← online help
    privacy.html      ← privacy policy
    support.html      ← support page
    images/           ← PNG assets
    videos/           ← MP4 demos
    docs/             ← audit reports and project memory
    LICENSE
    README.md


## 4. Audit rules


- The site must stay consistent with AGENTS.md section 1 at all times.
- When the plugin changes (name, version, commands, URLs), re-run the
  audit checklist in docs/AUDIT.md and update the site.
- Orphan images are allowed only if listed in docs/AUDIT.md whitelist.
- Never invent product features, commands, or URLs. If unsure, ask.


## 5. Git safety


- Push authorized when the task explicitly asks for it.
- Do not: force-push, reset --hard, delete branches, rewrite history,
  or create remote PRs/issues/releases.


## 6. Docs


- docs/AUDIT.md            ← audit checklist (canonical)
- docs/AUDIT_REPORT_*.md   ← dated audit results
- docs/DECISIONS.md        ← dated decision log (append-only)
---
