# ScatterFormer: Locally-Invariant Scattering Transformer for Patient-Independent Multispectral Detection of Epileptiform Discharges 

*AAAI 2023 Oral Presentation*

**Authors:**  
Ruizhe Zheng, Jun Li, Yi Wang, Tian Luo, **Yuguo Yu†**  
† *Corresponding author: [yuyuguo@fudan.edu.cn](mailto:yuyuguo@fudan.edu.cn)*  

*Fudan University*

📄 [Download PDF (AAAI)](https://openreview.net/forum?id=6Ve7wPSKvI))
---

## 🧩 Overview

**ScatterFormer** introduces a **Locally-Invariant Scattering Transformer** for **patient-independent multispectral detection of epileptiform discharges (EDs)**.  
It bridges *signal processing* and *transformer architectures* by integrating **wavelet-based scattering transforms** into a **hierarchical frequency-aware attention (FAA)** mechanism.  

Unlike standard CNN or ViT approaches that often lose high-frequency EEG information, ScatterFormer preserves **fine-grained spectral textures** essential for detecting subtle epileptic discharges across patients, channels, and time windows.

---

## 🚀 Highlights

- ⚙️ **Scattering-based Local Invariance**  
  Embeds wavelet scattering coefficients into Transformer tokens, offering translation and frequency robustness.

- 🌈 **Frequency-Aware Attention (FAA)**  
  Enables channel- and frequency-specific weighting for clinically meaningful feature localization.

- 🧠 **Patient-Independent EEG Detection**  
  Generalizes across subjects and sessions, eliminating the need for subject-specific retraining.

- 📈 **Explainability through Visual Spectra**  
  Provides interpretable attention maps correlated with high-frequency epileptiform bursts.

---

## 📊 Performance Summary

| Task | Dataset | Metric | Baseline | **ScatterFormer** | Gain |
|------|----------|---------|-----------|-------------------|------|
| Rolandic Epilepsy | In-house clinical EEG | AUCROC | 0.89 | **0.9814** | +9.1% |
| Rolandic Epilepsy | In-house clinical EEG | Accuracy | 0.87 | **0.9639** | +9.4% |
| Neonatal Seizure Detection | Helsinki Benchmark | AUCROC | 0.89 | **0.972** | +9.0% |

> ScatterFormer significantly improves patient-independent detection performance and interpretability over state-of-the-art baselines.

---

## 🧠 Method Overview


**Pipeline:**
1. Continuous EEG signals → Spectral Image Encoding  
2. Scattering Transform → Local invariant feature extraction  
3. Frequency-Aware Attention (FAA) → High-frequency refinement  
4. Transformer Encoder → Contextual integration  
5. Output: Epileptiform discharge probability map


