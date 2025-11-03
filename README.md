# Hybrid CNN–LSTM Framework for EEG Signal Classification

This repository presents a **research-based deep learning framework** for classifying multi-channel EEG signals of infants using hybrid **CNN–LSTM** and **CNN–Transformer** architectures.  
The project is part of an academic study focused on understanding early neural patterns related to **language acquisition and cognitive development**.

---

## 🧠 Overview

The dataset includes **48 preprocessed EEG segments** recorded from:
- 12 healthy infants (6 months)
- 12 language-impaired infants (6 months)
- 12 healthy infants (12 months)
- 12 language-impaired infants (12 months)

Due to ethical and privacy considerations, only **an anonymized single-sample dataset** is included in this repository for structural demonstration purposes.

---

## ⚙️ Methodology

### 1. Preprocessing
- Normalization of EEG signals in range [0, 1]  
- Band-pass filtering and motion artifact removal  
- Temporal segmentation into fixed-length epochs  
- Class-wise labeling for four subject categories  

### 2. Model Architecture
The framework integrates multiple hybrid approaches:
- **CNN layers** for spatial feature extraction across EEG channels  
- **LSTM layers** for capturing temporal dependencies  
- **Transformer encoder** (experimental) for attention-based sequence modeling  

### 3. Training Setup
| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Dropout Rate | 0.2 |
| Batch Size | 32 |
| Epochs | 20 |
| Validation Accuracy | ~85% (on limited validation subset) |

---

## 🔬 Research Context

This study explores how deep learning models can reveal **spatio-temporal brain activity patterns** related to early cognitive and language development in infants.  
It combines concepts from:
- **Computational Neuroscience**
- **Signal Processing**
- **Self-Supervised Learning for Time-Series Data**

The research involves an extensive literature review of **300+ scientific papers** in EEG-based developmental analysis, self-supervised learning, and hybrid deep architectures.

---

## ⚠️ Data Availability

The original EEG datasets cannot be shared publicly due to ethical restrictions and research confidentiality.  
However, a representative example is included in the notebook for reproducibility and transparency of the analytical process.

---

## 📘 Citation

> Alemzadeh, Y. (2025). *Hybrid CNN–LSTM Framework for EEG Signal Classification: A Deep Learning Study on Infant Brain Signals*.  
> Shahid Beheshti University, Tehran, Iran.

---

## 🧠 Author

**Yasamin Alemzadeh**  
B.Sc. in Computer Science, Shahid Beheshti University  
📧 yasaminalemzadeh541@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/yasamin-alemzadeh-860a31220)

