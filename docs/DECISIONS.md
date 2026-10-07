---
# Decisions — sheetset-excel-editor


Append-only. Newest first or oldest first — pick one and keep it.


## 2026-10-07 — Initial audit + memory structure


- Context: First audit of the site after the plugin was refactored
  (net10, 4 commands, validation integrated into SSEIMPORT).
- Decision:
  * Keep product name "Sheet Set Excel Editor" (no "for AutoCAD").
  * Keep version 1.0.0.
  * Keep orphan images validate.png, custom-property-creation.png,
    DATA-MODIFICATION.png for now (documented in docs/AUDIT.md whitelist).
  * Add meta description and Open Graph tags to the 4 pages.
  * Add AGENTS.md + docs/AUDIT.md + docs/DECISIONS.md.
- Impact: docs/ folder created; 4 HTML files updated.
- Status: applied.

## 2026-10-07 — Suppression de validate.png

- Context: L'image validate.png référençait une commande retirée
  (SSEVALIDATEXLSX, intégrée à SSEIMPORT).
- Decision: Supprimer définitivement images/validate.png.
- Impact: 1 fichier supprimé, whitelist AUDIT.md mise à jour.
- Status: applied.
---
