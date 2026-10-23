# Audit local — harmonisation visuelle — 2026-10-23

## Périmètre et résultat

**OK — modifications et vérifications locales terminées.**

Projet identifié par `CNAME` (`cad.lessard.xyz`), README et dépôt distant :
`elessard84/sheetset-excel-editor`.
Référence visuelle examinée en lecture seule :
`src/pages/index.astro` et `public/` dans le projet du site principal.

Les quatre pages restent statiques, en anglais, avec leurs styles intégrés.
Aucune dépendance d'exécution ajoutée. Les outils de vérification ont été
installés dans le répertoire temporaire OpenCode, hors des deux dépôts.

## Modifications visuelles

- En-têtes bleu nuit `#101d2a`, dégradé `#1d3b59`, texte clair `#eaf2fb`.
- Même pile typographique que le site principal :
  `Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`.
  Aucune police téléchargée.
- Bandeau développeur compact avec `images/logo-dark-bg.png` : environ 65 px
  sur l'accueil mobile et 64 px sur les pages secondaires mobiles.
- Logo produit existant distinct dans un panneau clair sur l'accueil.
- Boutons Videos et Screenshots bleus `#1362a3`, arrondis 8 px ; liens Help,
  Support et Privacy Policy secondaires, regroupés séparément sur mobile.
- Contenus clairs, cartes et blocs arrondis, bordures et espacements harmonisés.
- Favicons clair et sombre repris du site principal.
- Pieds de page sans logo, avec copyright et lien vers le site développeur.
- Tableau existant conservé avec `thead`, `tbody` et en-têtes `scope="col"`.

## Vérifications de conservation

Comparaison automatique avec les pages de `HEAD`, au moyen de leur DOM :

| Page | Texte du contenu principal | Texte d'en-tête existant | URL existantes vérifiées | Ancres conservées |
| --- | --- | --- | --- | --- |
| index.html | Identique | Identique hors nouveau bandeau | 20 | 3 |
| help.html | Identique | Identique hors nouveau bandeau | 13 | 9 |
| support.html | Identique | Identique hors nouveau bandeau | 7 | 0 |
| privacy.html | Identique | Identique hors nouveau bandeau | 4 | 0 |

La comparaison textuelle normalise uniquement les espaces. Aucun fichier
image ou vidéo préexistant n'est modifié. Les URL Open Graph sont conservées.

## Checklist canonique (`docs/AUDIT.md`)

| Contrôle | Résultat | Détail |
| --- | --- | --- |
| 1. Nom du produit | OK | Sheet Set Excel Editor conservé dans les quatre pages ; titres contextuels des pages secondaires préservés. |
| 2. Version | OK | 1.0.0 sur les pages qui affichent une version. |
| 3. Commandes | OK | Export, Import, About et Help conservés ; aucune commande de validation autonome ajoutée. |
| 4. Workflow | OK | Aide inchangée : export, édition, fermeture d'Excel, revue et confirmation de l'import, sauvegarde DST automatique. |
| 5. URL et liens | OK | Liens et ancres existants conservés ; destinations internes valides ; liens publics testés. |
| 6. Images | OK | Toutes les images référencées sont chargées. Nouveau logo référencé sur les quatre pages. Images orphelines existantes couvertes par la whitelist. |
| 7. Vidéos | OK | Trois sources accessibles ; métadonnées chargées et lecture effective vérifiée dans Chrome. |
| 8. Métadonnées | OK | Descriptions uniques et balises Open Graph conservées ; thème et favicons ajoutés. |
| 9. Cohérence interpages | OK | Identité, palette, typographie et signature harmonisées ; liens de pied de page contextuels existants conservés. |
| 10. Rapport | OK | Présent document et captures de revue visuelle. |

## Tests locaux

- **HTML : OK**, aucune erreur avec `html-validate` et les conventions adaptées
  au HTML existant. L'avertissement préexistant sur l'absence de `tbody` est corrigé.
- **CSS : OK**, analyse et validation des déclarations avec `css-tree`.
- **Responsive : OK**, quatre pages contrôlées à 320, 375, 390, 640, 768 et
  1440 px de largeur dans Chrome headless piloté par Playwright : 24 cas,
  aucun débordement horizontal, aucune image non chargée.
- **Ressources locales : OK**, 41 références internes contrôlées, toutes en HTTP 200.
- **Navigation : OK**, clics sur Videos et Screenshots avec arrivée sur la
  section correspondante, et sur Commands dans l'aide.
- **Vidéos : OK**, lecture effective des trois vidéos ; durées détectées
  d'environ 11,93 s, 30,97 s et 48,58 s.
- **Clavier : OK**, premier lien accessible au clavier avec focus visible.
- **Navigateur : OK**, aucune exception JavaScript ni réponse HTTP en erreur
  pendant la navigation locale.
- **Comparaison visuelle : OK**, accueil et aide examinés sur ordinateur et
  mobile ; même pile typographique et même couleur calculée des boutons
  principaux que le site vitrine. La référence a été rendue depuis son source
  en mémoire, sans compiler ni modifier le dépôt vitrine.
- **Liens publics : OK**, HTTP 200 pour `https://www.lessard.xyz/`,
  `https://cad.lessard.xyz/`, `help.html`, `support.html` et `privacy.html`
  sur le domaine CAD. Ce contrôle de disponibilité concerne les pages déjà
  publiées, pas les modifications locales.
- **Compilation : N/A**, le site CAD n'a aucune étape de compilation ; son
  workflow GitHub Pages publie directement les fichiers statiques.

## Accessibilité des informations Autodesk

**OK.** Compatibilité AutoCAD et produits verticaux 2026/2027, version 1.0.0,
nom du produit, auteur, aide, support, adresse de contact et politique de
confidentialité sont conservés. L'accès aux démonstrations et captures est
maintenu depuis l'en-tête de l'accueil.

## Captures

Captures du haut des pages, réalisées localement :

| Page | Ordinateur — 1440 × 1000 | Mobile — 390 × 844 |
| --- | --- | --- |
| Accueil | [Capture](visual-review-2026-10-23/home-desktop.png) | [Capture](visual-review-2026-10-23/home-mobile.png) |
| Aide | [Capture](visual-review-2026-10-23/help-desktop.png) | [Capture](visual-review-2026-10-23/help-mobile.png) |

## Revue visuelle finale avant publication

**OK — les quatre captures ont été réexaminées. Aucune retouche nécessaire.**

- Accueil ordinateur : bandeau LE secondaire, logo produit distinct et titre
  Sheet Set Excel Editor dominant ; boutons principaux et liens secondaires
  clairement différenciés. Sections visibles lisibles et bien espacées.
- Accueil mobile : identité développeur compacte, logo produit bien visible,
  titre lisible et navigation répartie en deux groupes cohérents.
- Aide ordinateur : bandeau LE discret, titre produit dominant, navigation
  interne lisible et hiérarchie des sections claire.
- Aide mobile : en-tête compact, liens sur plusieurs lignes sans chevauchement,
  paragraphes et titres visibles lisibles sur fond clair.

L'inventaire Git a été contrôlé : aucun script de test, dépendance de test,
journal, fichier temporaire ou configuration locale ajouté au projet.
Les quatre captures et les documents de revue sont des éléments de
documentation conservés volontairement dans le dépôt. Le workflow actuel
publiant la racine du projet, cette documentation sera également incluse
dans l'artefact du site.

## Contrôle des documents publics

Les rapports et les quatre captures ont été contrôlés avant publication.
Les chemins locaux des rapports récent et historique ont été remplacés par
des références relatives ou des identifiants publics. Les captures montrent
uniquement le contenu public des pages, sans barre d'adresse ni information
personnelle locale. Aucun secret ni identifiant d'authentification n'y figure.

## Statut au terme de la revue prépublication

Publication autorisée par le propriétaire après validation de la revue finale.
Les 14 fichiers de l'harmonisation sont conservés, avec une correction
supplémentaire du rapport historique pour retirer ses chemins locaux :
15 fichiers prévus dans le commit.
Le dépôt vitrine, les DNS, Cloudflare et le workflow de publication sont inchangés.
Le déploiement et les contrôles en ligne seront suivis après le push autorisé.
