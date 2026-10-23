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

## 2026-10-07 — Audit de synchro avec PRODUCT_FACTS.md

- Contexte : PRODUCT_FACTS.md créé dans SheetSetManager comme
  source de vérité unique.
- Décision : audit du site confirmé IN SYNC, aucune correction requise.
- Impact : aucun changement HTML. La procédure de synchro est
  désormais documentée dans PRODUCT_FACTS.md §8.
- Statut : IN SYNC.

## 2026-10-23 — Harmonisation visuelle avec www.lessard.xyz

- Contexte : harmonisation validée par le propriétaire après examen des deux
  projets locaux et confirmation du CNAME du site CAD.
- Décision : reprendre le bleu nuit, les accents bleus, la pile typographique
  système et les composants visuels du site principal, avec des contenus clairs.
  Garder le bandeau LE compact et le logo produit distinct sur l'accueil.
  Utiliser le symbole pour fond sombre uniquement dans les en-têtes ; aucun
  symbole LE n'est affiché sur fond clair ni répété dans les pieds de page.
  Les pieds de page portent « © 2026 Etienne Lessard », avec un lien vers
  https://www.lessard.xyz/. Réutiliser les deux favicons du site principal.
- Impact : présentation des quatre pages, trois nouvelles ressources graphiques,
  structure sémantique du tableau et documentation de la vérification locale.
  Contenu produit, URL, ancres et ressources existantes conservés.
- Statut : appliqué et testé localement ; validation finale requise avant
  commit, push ou déploiement.
---
