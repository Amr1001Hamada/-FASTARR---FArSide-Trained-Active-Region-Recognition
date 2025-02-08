# FASTARR: Far-Side Trained Active Region Recognition

## Overview
FASTARR (**FArSide Trained Active Region Recognition**) is a deep learning-based model designed for detecting solar far-side active regions (ARs) using helioseismic phase-shift maps. This model enhances space weather forecasting by identifying active regions before they rotate to the Earth-facing side.

FASTARR utilizes a U-Net architecture and is trained with two different datasets [Dual Training Approac]:
- FASTARR-G: Trained with AR masks derived from GONG phase-shift measurements.
- FASTARR-E: Trained with AR masks derived from STEREO/EUVI observations.

This repository provides the necessary scripts, pre-trained models, and dataset **samples** to train, evaluate, and use FASTARR for far-side AR detection.

## Repository Structure
```
FASTARR/
│── data/
│   ├── phase_shift_maps/      # Raw input phase-shift maps (GONG)
│   ├── GONG/AR_masks          # AR binary maps based on GONG measurements
│   ├── EUV/AR_masks           # AR binary maps based on EUV observations
│   ├── STEREO/EUV maps/       # Far-side EUV observations (as reference)
│
│── models/
│   ├── FASTARR_G/             # Trained model using GONG AR masks
│   ├── FASTARR_E/             # Trained model using EUV AR masks
│
│── src/
│   ├── UNet_func_of_blocks.py # U-Net model implementation
│
│── notebooks/
│   ├── FASTARR_G_training.ipynb   # Jupyter Notebook for FASTARR-G training
│   ├── FASTARR_G_Output.ipynb     # Jupyter Notebook for FASTARR-G predictions
│   ├── FASTARR_E_training.ipynb   # Jupyter Notebook for FASTARR-E training
│   ├── FASTARR_E_Output.ipynb     # Jupyter Notebook for FASTARR-E predictions
│
│── results/
│   ├── predictions/           # Example results on unseen data
│   ├── metrics/               # Performance reports & visualizations
│
│── docs/
│   ├── methodology.md         # Detailed explanation of the approach
│   ├── citation.md            # Citation & reference details
│
│── requirements.txt           # Python dependencies
│── LICENSE                    # Open-source license
```


## Citation
If you use FASTARR in your research, please cite:
> Hamada et al., "FASTARR: ***************** TBD

---
