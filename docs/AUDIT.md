---
# Audit checklist — sheetset-excel-editor


This checklist is the canonical audit procedure for the site.
Run it whenever the plugin changes or at least before any release.


## 1. Product name


- [ ] Every page shows "Sheet Set Excel Editor" (no "for AutoCAD").
- [ ] Page titles and <h1> match the product name.


## 2. Version


- [ ] Every page displaying a version shows 1.0.0.
- [ ] Update this checklist when a new version is released.


## 3. Commands


- [ ] Only SSEXPORT, SSEIMPORT, SSEABOUT, SSEHELP are mentioned.
- [ ] No mention of SSEVALIDATEXLSX, SSEAPPLYXLSXSETUP,
      SSEVERIFYXLSXSETUP, or a standalone "Validate" command.
- [ ] The workflow describes validation as integrated into SSEIMPORT.


## 4. Workflow


- [ ] The described workflow is: Export → Edit in Excel → Close Excel
      → Import (review + confirm) → automatic DST backup.
- [ ] No obsolete step (e.g. a separate validation command).


## 5. URLs and links


- [ ] cad.lessard.xyz, help.html, privacy.html, support.html links
      are correct and reachable.
- [ ] support@lessard.xyz is the support email.
- [ ] No broken internal links.


## 6. Images


- [ ] Every <img src="images/..."> reference resolves to an existing file.
- [ ] Orphan images in images/ are listed in the whitelist below.


### Whitelist (orphan images kept intentionally)


- validate.png (retained for archive; not used in current workflow)
- custom-property-creation.png (kept for future use)
- DATA-MODIFICATION.png (kept for future use)


## 7. Videos


- [ ] Every <video><source src="videos/..."> reference resolves
      to an existing file.
- [ ] Videos play and are up to date.


## 8. Metadata


- [ ] Every page has a unique <meta name="description">.
- [ ] Every page has Open Graph tags (og:title, og:description,
      og:image, og:url, og:type).


## 9. Cross-page consistency


- [ ] Product name, version, and URLs are identical across pages.
- [ ] Footer links are consistent.
- [ ] Support email is consistent.


## 10. Report


- [ ] Write results to docs/AUDIT_REPORT_YYYY-MM-DD.md.
- [ ] List every check with OK / KO / N/A.
- [ ] For every KO: file, line, snippet, suggested fix.
---
