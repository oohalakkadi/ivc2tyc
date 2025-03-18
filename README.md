# **Rerouting Connection: Hybrid Computer Vision Analysis Reveals Visual Similarity Between Indus and Tibetan-Yi Corridor Writing Systems**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Google Colab](https://img.shields.io/badge/Google-Colab-green?style=flat&logo=google)](https://drive.google.com/drive/folders/12opOs8jCRgwZ-GDaFyPSiCF-HBVQvuCO?usp=drive_link)
![Last Updated](https://img.shields.io/badge/Last%20Updated-2025--03--18-blue)

## **Abstract**

This thesis employs a hybrid CNN-Transformer architecture, in conjunction with a detailed anthropological framework, to investigate potential historical connections between the visual morphology of the Indus Valley script and pictographic systems of the Tibetan-Yi Corridor. Through an ensemble methodology of three target scripts across 15 independently trained models, we demonstrate that Tibetan-Yi Corridor scripts exhibit approximately six-fold higher visual similarity to the Indus script (61.7%-63.5%) than to the Bronze Age Proto-Cuneiform (10.2%-10.9%) or Proto-Elamite (7.6%-8.7%) systems. 

Additionally, in contrary with our current understanding of the networks of the Indus Valley Civilization, the Indus script unexpectedly maps closer to Tibetan-Yi Corridor scripts, with a mean cosine similarity of 0.629, than to the aforementioned contemporaneous West Asian signaries, both of which recorded mean cosine similarities of 0.104 and 0.080 despite their close geographic proximity and evident trade relations. Across various dimensionality reduction practices and clustering methodologies, the Indus script consistently clusters closest to Tibetan-Yi Corridor scripts. 

Our computational results align with qualitative observations of specific pictorial parallels in numeral systems, gender markers, and key iconographic elements; this is further supported by archaeological evidence of sustained contact networks along the ancient Shu-Shendu road in tandem with the Indus Valley Civilization's decline, providing a plausible transmission pathway. While alternative explanations cannot be ruled out, the specificity and consistency of observed similarities challenge conventional narratives of isolated script development and suggest more complex ancient cultural transmission networks between South and East Asia than previously recognized.

## **Repository Structure**

This repository (`oohalakkadi/ivc2tyc`) contains all code, datasets, and supplementary materials for this thesis project. 

```plaintext
ivc2tyc/
├── notebooks/
│   ├── script_analysis.ipynb          # Main notebook with core analysis
│   ├── datasets.ipynb                 # Used to load data into Google Drive
│   └── old_naxi.ipynb                 # Specialized notebook for Old Naxi dataset
│
├── datasets/                          # Contains all datasets as saved to Google Drive
│   ├── indus/                         # Indus Valley script characters
│   ├── proto_cuneiform/               # Proto-Cuneiform script characters
│   ├── proto_elamite/                 # Proto-Elamite script characters
│   ├── ba-shu/                        # Ba-Shu/Sanxingdui script characters
│   ├── yi/                            # Classical Yi script characters
│   ├── standard_yi/                   # Standardized Yi script characters
│   ├── naxi_dongba/                   # Newer Dongba script characters
│   └── old_naxi/                      # Older Dongba script characters
│
├── figures/                           # Visualizations and diagrams
│   ├── cosine_similarity/             # Cosine similarity visualizations
│   ├── t-sne/                         # t-SNE dimensionality reduction plots
│   ├── pca/                           # PCA dimensionality reduction plots
│   ├── dendrograms/                   # Hierarchical clustering dendrograms
│   ├── grad-cam/                      # Grad-CAM visualizations
│   ├── diagrams/                      # Custom diagrams
│   ├── training/                      # Ensemble training data and visualizations
│   ├── clustered_heatmaps/            # Clustered heatmap visualizations
│   ├── statistical_tests.csv          # Statistical test data
│   └── similarity_summary.md          # Summary of similarity scores
│
├── reference/                         # Reference datasets loaded from this repository
│   ├── indus/                         # Indus Valley reference materials
│   └── tyc/                           # Tibetan-Yi Corridor reference materials
│
├── stability_analysis/                # Leave-out testing, t-tests, Cohen's d
│
├── paper/                             # Final thesis paper and components
│   ├── main.tex                       # Main LaTeX document
│   ├── UndergraduateThesis.pdf        # Full PDF
│   └── bibfile.bib                 # Bibliography file
│
├── poster/                            # Thesis poster presentation materials
│   ├── FinalPoster.jpg                # Final poster JPG
│   └── FinalPoster.ai                 # Adobe Illustrator file
│
└── fonts/                             # Font files for document consistency
    └── source-serif-pro/              # Source Serif Pro font files
```

### *Notebooks*

The `notebooks` directory contains three Jupyter notebooks created in Google Colab:

- `script_analysis.ipynb` – The main notebook containing the core analysis
- `datasets.ipynb` – Used to load and preprocess data into Google Drive for access by `script_analysis.ipynb`
- `old_naxi.ipynb` – Specialized notebook for handling the Old Naxi dataset

### *Datasets*

The `datasets` folder contains all datasets as they were saved to Google Drive. These datasets are used for training and evaluating the models. Reference datasets used in the notebooks are stored in the `reference` directory.

### *Figures*

The `figures` directory contains:

- All visualizations generated by the analysis
- Custom diagrams created to illustrate key concepts and qualitative observations

### *Stability Analysis*

The `stability_analysis` directory contains:

- Data and graphs from leave-out testing
- Welch's t-test results
- Cohen's d effect size calculations

### *Paper and Poster*

- `paper` – Contains the final thesis paper
- `poster` – Contains the thesis poster presentation materials

### *Additional Resources*

- `fonts` – Contains Source Serif Pro font files used throughout all materials
- `reference` – Contains reference datasets loaded directly from this repository

## **External Resources**
Due to size constraints, the following resources are hosted on Google Drive:

[Trained Models (15 total)](https://drive.google.com/drive/folders/15YeGHhwdYd3NClnDWDG_aCqoSTC2H_SZ)

[Extracted Feature Embeddings](https://drive.google.com/drive/folders/1--2eYvjJNlu0G_iY84B0xUZsP7eNbjTC)

[Complete Drive Directory](https://drive.google.com/drive/folders/1hmO5IDxNRJenfmWwpJuhRXcs6rNc8MyD)

## **Setup and Usage**

1. Clone this repository into your Colab environment

  ```python
  from google.colab import drive
   rive.mount('/content/drive')
   
  %cd /content/
  !git clone https://github.com/oohalakkadi/ivc2tyc.git
  ```
2. Run notebooks in the following order within Google Colab:
  - For Old Naxi specific loading and processing, run `old_naxi.ipynb`
  - Run `datasets.ipynb` to load the rest of the data
  - Run the main analysis in `script_analysis.ipynb`


## **Institutional Context**

This thesis was completed as part of the Signature Work program at Duke Kunshan University (DKU), an interdisciplinary institution that grants dual undergraduate degrees from DKU and Duke University.

## **Citation**

If you use this work in your research, please cite:

```bibtex
@undergraduatethesis{Reddy2025,
  author       = {Reddy, Ooha},
  title        = {Rerouting Connection: Hybrid Computer Vision Analysis Reveals Visual Similarity Between Indus and Tibetan-Yi Corridor Writing Systems},
  school       = {Duke Kunshan University},
  year         = {2025},
  month        = {March},
  url          = {https://github.com/oohalakkadi/ivc2tyc}
}
```

## **License**

This project is licensed under the MIT License.