# Audit du site web — Sheet Set Excel Editor

- **Date :** 2026-10-07
- **Dépôt :** `D:\Documents\GitHub\sheetset-excel-editor`
- **Site :** https://cad.lessard.xyz (GitHub Pages, `CNAME` = `cad.lessard.xyz`)
- **Produit :** Sheet Set Excel Editor v1.0.0 (Etienne Lessard)
- **Mode :** lecture seule — aucune modification des fichiers HTML/images/vidéos.

## Tableau récapitulatif

| # | Point vérifié | Statut | Détail |
|---|---|---|---|
| 1 | Nom produit « Sheet Set Excel Editor » (sans « for AutoCAD ») | OK | Aucune occurrence de « for AutoCAD » |
| 2 | Commandes (pas de SSEVALIDATEXLSX/SSEAPPLYXLSXSETUP/SSEVERIFYXLSXSETUP/Validate) | OK | Aucune mention des commandes retirées |
| 3 | Workflow (export → edit → close Excel → import + validation intégrée → backup) | OK | Cohérent avec le code actuel |
| 4 | URLs et liens cohérents | OK* | *1 incohérence cosmétique (help.html:105) |
| 5 | Images référencées vs images/ | KO | 3 images orphelines (dont `validate.png`) |
| 6 | Vidéos référencées vs videos/ | OK | 3 référencées, 3 existantes, 0 orpheline |
| 7 | Cohérence inter-pages (nom, version, URLs) | OK | Uniforme sur index/help/support/privacy |
| 8 | Version produit = 1.0.0 | OK | 1.0.0 partout, aucune « 1.0 » seule |
| 9 | Métadonnées HTML (title/meta/OG) | KO | `<title>` OK ; `meta description` + OG absents |

Légende : OK = conforme · KO = anomalie à corriger · * = conforme avec remarque mineure.

## Anomalies détaillées (KO / remarques)

### 5. Images orphelines (présentes dans images/ mais non référencées)

| Fichier orphelin | Commentaire | Correction suggérée |
|---|---|---|
| `images/validate.png` | Bouton « Validate » retiré du plugin ; plus référencé. | Supprimer du dépôt (ou réutiliser si le workflow change). |
| `images/custom-property-creation.png` | Jamais référencé. | Ajouter une section « Create Custom Properties » dans les screenshots, ou supprimer. |
| `images/DATA-MODIFICATION.png` | Jamais référencé. | Ajouter comme capture « Edit in Excel », ou supprimer. |

Aucune référence cassée : les 7 images référencées dans `index.html` existent toutes dans `images/`.

### 4. Lien cosmétiquement incohérent — `help.html:105`

- **Extrait :** `<a href="privacy.html">https://cad.lessard.xyz/privacy.html</a>`
- **Problème :** le texte affiché est l'URL absolue, mais le `href` est relatif (`privacy.html`). Fonctionne, mais incohérent.
- **Correction suggérée :** aligner le texte sur les autres liens, ex. `<a href="privacy.html">Privacy Policy</a>`.

### 9. Métadonnées manquantes — toutes les pages

- **Extrait :** aucune balise `<meta name="description" ...>`, aucun Open Graph (`og:title`, `og:image`…) ni Twitter Card.
- **Problème :** aperçu social / SEO minimal.
- **Correction suggérée :** ajouter sur les 4 pages :
  ```html
  <meta name="description" content="Export, edit and import AutoCAD Sheet Set data using Excel. Sheet Set Excel Editor.">
  <meta property="og:title" content="Sheet Set Excel Editor">
  <meta property="og:description" content="Export, edit and import AutoCAD Sheet Set data using Excel.">
  <meta property="og:image" content="https://cad.lessard.xyz/images/ssee_logo.png">
  <meta property="og:url" content="https://cad.lessard.xyz/">
  <meta property="og:type" content="website">
  ```

## Remarques (non bloquantes)

- **Commandes non nommées explicitement :** le site documente les 4 commandes par leur libellé (Export / Import / About / Help) mais n'affiche nulle part les noms de commande réels `SSEXPORT`, `SSEIMPORT`, `SSEABOUT`, `SSEHELP`. Aucune des commandes retirées n'est mentionnée (conforme). Suggestion : indiquer les noms de commande dans `help.html` (section « Ribbon Commands ») pour cohérence totale avec le code.
- **Workflow :** `index.html:51` résume bien « DST → Export XLSX → Edit in Excel → Review in Import → Confirm → DST » ; `help.html:42-53` inclut explicitement l'étape « Close Excel » (l.49) et le backup automatique (l.52). La validation est intégrée à l'import (« Review in Import »), sans étape « Validate » séparée — conforme.
- **« validation » (index.html:46) :** mentionne « maintaining validation and import controls » — fait référence à la validation intégrée à l'import, pas à une commande retirée. Non problématique.

## Résumé (10 lignes)

1. Nom produit uniforme « Sheet Set Excel Editor », aucune trace de « for AutoCAD ».
2. Aucune mention des commandes retirées (SSEVALIDATEXLSX, SSEAPPLYXLSXSETUP, SSEVERIFYXLSXSETUP, Validate).
3. Workflow conforme : export → édition Excel → fermeture Excel → import avec revue/validation intégrée → backup auto.
4. Version 1.0.0 affichée partout (index, help, support).
5. URLs cohérentes (cad.lessard.xyz, support@lessard.xyz) ; 1 incohérence cosmétique sur help.html:105.
6. Images : 7 référencées, toutes présentes ; 3 orphelines dont `validate.png` (à supprimer).
7. Vidéos : 3 référencées, 3 présentes, aucune orpheline.
8. Cohérence inter-pages parfaite (nom, version, auteur, contacts).
9. Métadonnées : `<title>` corrects ; `meta description` et Open Graph absents sur les 4 pages.
10. Seules actions recommandées : supprimer `validate.png` (+ 2 images orphelines), ajouter `meta description`/OG, harmoniser le libellé de lien help.html:105.
