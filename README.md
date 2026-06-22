# Hybrid CNN–LSTM Framework for EEG Signal Classification

> A research-based deep learning framework for classifying multi-channel EEG signals of infants using hybrid CNN–LSTM and CNN–Transformer architectures, focused on early neural patterns related to language acquisition and cognitive development.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active%20Research-brightgreen)
![Literature](https://img.shields.io/badge/Literature%20Review-300%2B%20Papers-blueviolet)

---

## Overview

This project investigates how deep learning models can reveal spatio-temporal brain activity patterns tied to early cognitive and language development in infants. It brings together **Computational Neuroscience**, **Signal Processing**, and **Self-Supervised Learning for Time-Series Data**.

The dataset comprises **48 preprocessed EEG segments** recorded from four subject groups:

| Group | Age | n |
|-------|-----|---|
| Healthy infants | 6 months | 12 |
| Language-impaired infants | 6 months | 12 |
| Healthy infants | 12 months | 12 |
| Language-impaired infants | 12 months | 12 |

> ⚠️ Due to ethical and privacy considerations, only an anonymized single-sample dataset is included in this repository for structural demonstration. The full EEG dataset cannot be shared publicly.

---

## Methodology

### 1 · Preprocessing

- Normalization of EEG signals to the range [0, 1]
- Band-pass filtering and motion artifact removal
- Temporal segmentation into fixed-length epochs
- Class-wise labeling across four subject categories

### 2 · Architecture

```
Raw Multi-Channel EEG
        │
        ▼
┌──────────────────────┐
│    Preprocessing     │
│  Normalize · Filter  │
│  Segment · Label     │
└──────────┬───────────┘
           │
   ┌───────┴────────┐
   ▼                ▼
CNN Layers      CNN Layers
(spatial        (spatial
 features)       features)
   │                │
   ▼                ▼
LSTM Layers    Transformer
(temporal      Encoder
 context)      (attention)
   │                │
   └───────┬────────┘
           ▼
   Classification Head
   (4-class output)
```

Three architectures are evaluated in parallel:
- **CNN–LSTM** — spatial feature extraction followed by recurrent temporal modeling
- **CNN–Transformer** — spatial features fed into attention-based sequence modeling (experimental)
- **Standalone CNN / LSTM** — used as ablation baselines

### 3 · Training Setup

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Dropout Rate | 0.2 |
| Batch Size | 32 |
| Epochs | 20 |
| Validation Accuracy | ~85% *(limited validation subset)* |

---

## Research Context

This study sits at the intersection of:

- **Computational Neuroscience** — modeling infant brain activity from multi-channel EEG
- **Signal Processing** — robust preprocessing pipelines for noisy biosignals
- **Self-Supervised Learning** — representation learning strategies for time-series without full annotation

The project draws on an extensive literature review of **300+ scientific papers** covering EEG-based developmental analysis, hybrid deep architectures, and self-supervised learning for biomedical signals.

---

## Repository Structure

```
├── data/
│   └── sample/             # Anonymized single-sample dataset
├── notebooks/
│   └── eeg_classification.ipynb
├── models/
│   ├── cnn_lstm.py
│   └── cnn_transformer.py
├── preprocessing/
│   └── pipeline.py
└── README.md
```

---

## Citation

```bibtex
@misc{alemzadeh2025eeg,
  author      = {Alemzadeh, Yasamin},
  title       = {Hybrid CNN-LSTM Framework for EEG Signal Classification:
                 A Deep Learning Study on Infant Brain Signals},
  year        = {2025},
  institution = {Shahid Beheshti University, Tehran, Iran},
  url         = {https://github.com/Yasamin-Alemzadeh}
}
```

---

## Author

**Yasamin Alemzadeh**
M.Sc. Computer Science, TU Berlin · B.Sc. Computer Science, Shahid Beheshti University

[![Email](https://img.shields.io/badge/Email-yasaminalemzadeh541%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:yasaminalemzadeh541@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Yasamin%20Alemzadeh-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yasamin-alemzadeh-860a31220)
[![GitHub](https://img.shields.io/badge/GitHub-Yasamin--Alemzadeh-181717?style=flat&logo=github&logoColor=white)](https://github.com/Yasamin-Alemzadeh)
