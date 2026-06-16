# Zenodo Deposit Plan

This document describes the dedicated **code/data Zenodo deposit** to be created
for this project. As of this writing, that deposit **does not yet exist** — this
file is the preparation plan. Once the deposit is published, add its DOI to
`README.md`, `CITATION.cff`, and the manuscript's data availability statement.

> The preprint DOI `https://doi.org/10.5281/zenodo.20018003` refers to the
> **preprint** only. It is **not** the code/data archive DOI. The code/data
> archive is forthcoming and will receive its own DOI.

## Suggested archive components

Upload the following to the Zenodo deposit:

| File | Contents |
|------|----------|
| `ivc2tyc-code-v1.0.0.zip` | Notebooks and scripts (the runnable code). |
| `ivc2tyc-datasets-v1.0.0.zip` | Script character image datasets (`datasets/`, `reference/`), with per-source attribution. |
| `ivc2tyc-trained-models-v1.0.0.zip` | The 15 trained model checkpoints (`.pth`). |
| `ivc2tyc-embeddings-and-results-v1.0.0.zip` | Extracted feature embeddings, similarity matrices, statistical outputs, and complete generated figures/outputs. |
| `README.md` | This repository's README (top-level project documentation). |
| `LICENSE` | MIT License for the code, with third-party/data licensing notes. |
| `CITATION.cff` | Machine-readable citation metadata. |

Tip: you can also enable the **GitHub–Zenodo integration** and create a tagged
GitHub release (e.g. `v1.0.0`) so the code snapshot is archived automatically;
then upload the large datasets/models/embeddings artifacts to the same Zenodo
record manually (or as a new version).

## Recommended Zenodo metadata

**Title**

> Code and data for: Quantifying Structural Similarity between Indus and
> Tibetan–Yi Scripts Using Hybrid Vision Embeddings

**Creator**

> Ooha Lakkadi Reddy

**Resource type**

> Software (with associated dataset files), or Dataset — Zenodo allows a primary
> type; "Software" is appropriate given the code-centric record. Use the
> related identifiers below to link the supporting data.

**Description**

> Code, datasets, trained models, extracted embeddings, and generated outputs
> supporting the PCI-recommended study *Quantifying Structural Similarity
> between Indus and Tibetan–Yi Scripts Using Hybrid Vision Embeddings*. The
> project uses a hybrid CNN–Transformer architecture to compare the visual
> morphology of the Indus Valley script with the pictographic writing systems
> of the Tibetan–Yi Corridor (including Naxi Dongba, Yi, and Ba–Shu symbols),
> benchmarked against Proto-Cuneiform and Proto-Elamite. The deposit contains
> the analysis notebooks, the script-character image datasets, the trained model
> ensemble, the extracted feature embeddings, and the complete set of similarity
> matrices, statistical results, and figures. Recommended by PCI Archaeology
> (https://doi.org/10.24072/pci.archaeo.100711).

**Keywords**

```
Indus script
Tibetan–Yi Corridor
Dongba script
Ba–Shu symbols
computational archaeology
computer vision
script comparison
visual embeddings
hybrid CNN Transformer
```

**Related identifiers**

| Relation | Identifier |
|----------|------------|
| `is supplement to` (PCI recommendation) | https://doi.org/10.24072/pci.archaeo.100711 |
| `is supplement to` / `is derived from` (preprint) | https://doi.org/10.5281/zenodo.20018003 |
| `is supplement to` (source code repository) | https://github.com/oohalakkadi/ivc2tyc |

## License guidance

- **Code:** MIT.
- **Third-party datasets:** retain their original licenses and source
  attribution; do **not** relicense them. Document each source in the dataset
  archive.
- **Newly generated outputs** (figures, embeddings, derived tables): choose
  **CC BY 4.0** unless there is a specific reason not to.

Because Zenodo records carry a single license field, consider setting the record
license to MIT (or CC BY 4.0) and including a clear `LICENSE`/`NOTICE` file
inside the archives that spells out the mixed licensing above.

## After publishing

1. Copy the minted DOI.
2. Replace `Dedicated code/data Zenodo archive: forthcoming` in `README.md` with
   the DOI (and add a DOI badge).
3. Add the DOI to `CITATION.cff` (`doi:` and/or `identifiers:`).
4. Update the manuscript's data availability statement.
5. Tick the corresponding items in `ARCHIVAL_CHECKLIST.md`.
