# Archival Release Checklist

A practical checklist for preparing this repository for archival release, Zenodo
deposition, the PCI Archaeology recommendation, and CAA Proceedings publication.

## Repository hygiene

- [x] `README.md` updated (archival, non-thesis-branded, Zenodo as source of record)
- [x] `CITATION.cff` present and valid
- [x] `LICENSE` present (MIT for code; third-party data attribution noted)
- [x] `requirements.txt` present
- [x] `.gitignore` covers caches, checkpoints, OS, and temp files
- [x] Google Drive references removed or reframed in documentation
      (Drive presented only as a development/Colab environment, not the archive)

## Zenodo code/data deposit

- [x] Code/data Zenodo deposit created (see `ZENODO_DEPOSIT_PLAN.md`)
- [x] Archive components uploaded
      (`ivc2tyc-code`, `ivc2tyc-datasets`, `ivc2tyc-trained-models`,
      `ivc2tyc-embeddings-and-results`, plus `README.md`, `LICENSE`, `CITATION.cff`)
- [x] Zenodo metadata set (title, creator, description, keywords, related identifiers, license)
- [x] Zenodo DOI minted — `10.5281/zenodo.20755243`
- [x] Zenodo DOI added back into `README.md` (replacing the "forthcoming" placeholder)
- [x] Zenodo DOI added to `CITATION.cff`

## GitHub release

- [ ] GitHub release created (e.g. tag `v1.0.0`)
- [ ] GitHub–Zenodo integration enabled (for automatic code-snapshot archiving)

## Manuscript / publication

- [ ] Manuscript data availability statement updated (points to Zenodo DOI)
- [ ] PCI Archaeology recommendation cited (https://doi.org/10.24072/pci.archaeo.100711)
- [ ] PCI badge / recommendation statement added to the PDF
- [ ] CAA Proceedings template applied / updated
