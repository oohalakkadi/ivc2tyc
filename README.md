# Quantifying Structural Similarity between Indus and Tibetan–Yi Scripts Using Hybrid Vision Embeddings

[![License: MIT](https://img.shields.io/badge/Code%20License-MIT-yellow.svg)](LICENSE)
[![PCI Archaeology](https://img.shields.io/badge/PCI%20Archaeology-Recommended-brightgreen.svg)](https://doi.org/10.24072/pci.archaeo.100711)

This repository contains the code, notebooks, figures, and selected reproducibility
materials for the study *Quantifying Structural Similarity between Indus and
Tibetan–Yi Scripts Using Hybrid Vision Embeddings*.

The project uses a hybrid CNN–Transformer architecture, together with an
anthropological framework, to investigate potential historical relationships
between the visual morphology of the Indus Valley script and the pictographic
writing systems of the Tibetan–Yi Corridor (TYC). Using an ensemble of
independently trained models across three target scripts, the study finds that
TYC scripts exhibit substantially higher visual similarity to the Indus script
than to the Bronze Age Proto-Cuneiform or Proto-Elamite systems, and that the
Indus script consistently clusters closest to TYC scripts across multiple
dimensionality-reduction and clustering methods.

## Peer Review and Recommendation Status

This work has been peer-reviewed and **recommended by [PCI Archaeology](https://archaeo.peercommunityin.org/)**
(Peer Community In Archaeology).

- **PCI Archaeology recommendation DOI:** https://doi.org/10.24072/pci.archaeo.100711

The recommended article is intended for publication in the *CAA Proceedings*
(Computer Applications and Quantitative Methods in Archaeology).

## Repository Structure

```plaintext
ivc2tyc/
├── notebooks/                  # Jupyter notebooks (developed for Google Colab)
│   ├── script_analysis.ipynb   # Main notebook: training, embeddings, analysis
│   ├── datasets.ipynb          # Dataset acquisition and preprocessing
│   └── old_naxi.ipynb          # Specialized processing for the Old Naxi dataset
│
├── datasets/                   # Script character image datasets
│   ├── indus/                  # Indus Valley script characters
│   ├── proto_cuneiform/        # Proto-Cuneiform script characters
│   ├── proto_elamite/          # Proto-Elamite script characters
│   ├── ba-shu/                 # Ba-Shu / Sanxingdui script characters
│   ├── yi/                     # Classical Yi script characters
│   ├── standard_yi/            # Standardized Yi script characters
│   ├── naxi_dongba/            # Naxi Dongba script characters
│   └── old_naxi/               # Older Naxi (Dongba) script characters
│
├── reference/                  # Reference materials used by the notebooks
│   ├── indus/                  # Indus Valley reference materials
│   └── tyc/                    # Tibetan–Yi Corridor reference materials
│
├── figures/                    # Generated visualizations and diagrams
│   ├── cosine_similarity/       # Cosine-similarity visualizations
│   ├── t-SNE/                   # t-SNE projections
│   ├── PCA/                     # PCA projections
│   ├── Dendrograms/             # Hierarchical clustering dendrograms
│   ├── Grad-CAM/                # Grad-CAM visualizations
│   ├── clustered_heatmaps/      # Clustered similarity heatmaps
│   ├── Training/                # Ensemble training curves and summaries
│   ├── diagrams/                # Custom explanatory diagrams
│   ├── statistical_tests.csv    # Statistical test results
│   └── similarity_summary.md    # Summary of similarity scores
│
├── stability_analysis/         # Leave-out testing, Welch's t-tests, Cohen's d
│
├── paper/                      # Manuscript and components
│   ├── UndergraduateThesis.pdf # PDF of the originating Signature Work product
│   └── LaTeX/                  # LaTeX sources, bibliography, and figures
│
├── poster/                     # Poster presentation materials
│
├── fonts/                      # Font files used for document consistency
│
├── requirements.txt            # Python dependencies
├── CITATION.cff                # Citation metadata
├── LICENSE                     # MIT License (code)
├── ZENODO_DEPOSIT_PLAN.md      # Plan for the dedicated Zenodo code/data archive
└── ARCHIVAL_CHECKLIST.md       # Release/archival checklist
```

## Setup and Usage

The analysis was developed in **Google Colab**, where Google Drive was used as a
working/scratch environment for mounting datasets, checkpoints, and intermediate
outputs. The notebooks therefore contain historical `/content/drive/...` paths
from that development workflow. To run the notebooks elsewhere, adjust those
paths to point to your local copy of the `datasets/` directory and a writable
output location.

### Dependencies

```bash
pip install -r requirements.txt
```

Dependencies are listed without strict version pins (see
[`requirements.txt`](requirements.txt)). The notebooks were run on a CUDA-enabled
GPU environment (Google Colab). For exact reproduction, install a `torch` /
`torchvision` build that matches your CUDA/CPU setup, and pin versions to those
recorded in your own environment if bit-for-bit reproducibility is required.

### Suggested run order

1. `old_naxi.ipynb` — extract and preprocess the Old Naxi dataset.
2. `datasets.ipynb` — acquire and preprocess the remaining datasets.
3. `script_analysis.ipynb` — train the model ensemble, extract embeddings, and
   produce the similarity analysis and figures.

## Data and Artifact Availability

This GitHub repository holds the code, notebooks, figures, smaller datasets, and
selected reproducibility materials. **Large research artifacts — trained model
checkpoints, extracted embeddings, and complete generated outputs — are intended
to be archived in a dedicated Zenodo code/data deposit**, which is the intended
long-term archival source of record for this project.

- **Dedicated code/data Zenodo archive: forthcoming**

See [`ZENODO_DEPOSIT_PLAN.md`](ZENODO_DEPOSIT_PLAN.md) for the planned contents
and metadata of that deposit. Once the Zenodo archive is created, its DOI will be
added here.

> **Note on Google Drive.** Google Drive was used only as a development and Colab
> working environment during the project. It is *not* the archival source of
> record. Any Google Drive paths or links remaining inside the notebooks reflect
> that original Colab workflow and are retained for historical transparency.

## Reproducibility Notes

- Training uses an ensemble of independently initialized models; exact numerical
  results may vary slightly across hardware, library versions, and random seeds.
- Reported similarity scores, statistical tests, and figures are included under
  `figures/` and `stability_analysis/` so that published results can be inspected
  without rerunning training.
- Full reproduction of the trained models and embeddings requires the artifacts
  planned for the dedicated Zenodo deposit (see above).

## Citation

If you use this work, please cite **both** the repository/data archive (once the
dedicated Zenodo DOI is available) **and** the PCI-recommended article.

Until the dedicated code/data Zenodo DOI is minted, please cite the repository
and the PCI Archaeology recommendation:

```bibtex
@software{LakkadiReddy_ivc2tyc,
  author  = {Lakkadi Reddy, Ooha},
  title   = {Code and data for: Quantifying Structural Similarity between
             Indus and Tibetan--Yi Scripts Using Hybrid Vision Embeddings},
  version = {1.0.0},
  url     = {https://github.com/oohalakkadi/ivc2tyc},
  note    = {Recommended by PCI Archaeology,
             https://doi.org/10.24072/pci.archaeo.100711}
}
```

See [`CITATION.cff`](CITATION.cff) for machine-readable citation metadata.

## License

- **Code** (notebooks and scripts) is released under the [MIT License](LICENSE).
- **Third-party datasets** included or referenced here retain their **original
  licenses and source attribution**; they are *not* relicensed under MIT. Please
  consult the original sources before reuse and cite them appropriately.
- **Newly generated outputs** (figures, embeddings, derived tables) are intended
  to be released under CC BY 4.0 via the Zenodo deposit unless otherwise noted.

Bundled fonts retain their own licenses (e.g., the SIL Open Font License for
Source Serif Pro; see `fonts/source-serif-pro/`).

## Author and Contact

**Ooha Lakkadi Reddy**

- Repository: https://github.com/oohalakkadi/ivc2tyc

The originating Signature Work product was completed at Duke Kunshan University
(DKU), an interdisciplinary institution granting dual undergraduate degrees from
DKU and Duke University.
