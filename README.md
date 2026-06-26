# Stellar Population Classification in Open Clusters
## Using Unsupervised Machine Learning and Gaia DR3

[![DOI](https://zenodo.org/badge/DOI/YOUR_DOI_HERE.svg)](https://doi.org/YOUR_DOI_HERE)

**Author:** Nischal Shah
**Status:** Submitted to Young Scientists Journal (YSJ) | Preprint on Zenodo  
**Paper:** [View on Zenodo](https://zenodo.org/records/20822726)

---

## Overview

This repository contains the complete analysis pipeline for the study:

> *"Unsupervised Machine Learning Classification of Stellar Populations 
> in Open Clusters Using Gaia DR3 Photometry and Astrometry"*

We apply four unsupervised machine learning algorithms to Gaia DR3 photometric and astrometric data for four open clusters, identifying distinct stellar population substructure and validating results against PARSEC stellar evolution isochrones.

---

## Clusters Analyzed

| Cluster | Age       | Stars (after cleaning) |
|--------- |----------|------------------------|
| Pleiades | ~125 Myr | 1,055                  |
| Praesepe | ~700 Myr | 921                    |
| NGC 2516 | ~150 Myr | 2,836                  |
| Blanco 1 | ~100 Myr | 597                    |
| **Total** |         | **5,409**              |

---

## Methods

- **Data source:** ESA Gaia DR3 (queried via astroquery)
- **Quality cuts:** 5-step cleaning pipeline (parallax error ratio, 
  RUWE, parallax window, proper motion window, null removal)
- **ML algorithms:** K-means, DBSCAN (ε-optimized), 
  Gaussian Mixture Models (BIC-selected), Self-Organizing Maps
- **Validation:** Modified Silhouette Score, PARSEC isochrone overlay

---

## Key Results

1. Main sequence turnoff age-gradient recovered across all 4 clusters
2. NGC 2516 giant/supergiant candidates spontaneously detected
3. White dwarf candidates identified across multiple clusters
4. SOM U-Matrix density discontinuities reveal stellar population boundaries
5. Three-algorithm method comparison shows continuous main sequence 
   structure with no sharp discrete subpopulation boundaries

---

## Repository Structure
├── notebooks/
│   └── stellar_population_analysis_complete.ipynb
---

## How to Reproduce

```bash
# Clone this repository
git clone https://github.com/nischalcool/stellar-population-ml-gaia

# Install dependencies
pip install -r requirements.txt

# Run notebooks in order (01 through 08)
# All data is queried directly from Gaia DR3 in notebook 01
```

---

## Citation

If you use this code or pipeline, please cite:
Shah, N. (2025). Unsupervised Machine Learning Classification of Stellar Populations in Open Clusters Using Gaia DR3 Photometry and Astrometry. Zenodo. (https://zenodo.org/records/20822726)

---

## Contact

Nischal Shah | Independent Researcher | Dharan, Nepal  
Nischal Shah
