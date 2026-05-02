<div align="center">

```
███╗   ██╗███████╗██╗   ██╗██████╗  ██████╗ ██╗   ██╗██╗██████╗ ███████╗
████╗  ██║██╔════╝██║   ██║██╔══██╗██╔═══██╗██║   ██║██║██╔══██╗██╔════╝
██╔██╗ ██║█████╗  ██║   ██║██████╔╝██║   ██║██║   ██║██║██████╔╝█████╗  
██║╚██╗██║██╔══╝  ██║   ██║██╔══██╗██║   ██║╚██╗ ██╔╝██║██╔══██╗██╔══╝  
██║ ╚████║███████╗╚██████╔╝██║  ██║╚██████╔╝ ╚████╔╝ ██║██████╔╝███████╗
╚═╝  ╚═══╝╚══════╝ ╚═════╝ ╚═╝  ╚═╝ ╚═════╝   ╚═══╝  ╚═╝╚═════╝ ╚══════╝
```

### *Seeing what radiologists miss. Instantly.*

<br/>

[![](https://img.shields.io/badge/-%F0%9F%A7%A0%20Live%20Demo-000000?style=for-the-badge)](app.html)
[![](https://img.shields.io/badge/-Research%20Paper-1a1a2e?style=for-the-badge&logo=arxiv&logoColor=white)](#-citation)
[![](https://img.shields.io/badge/-93.1%25%20Accuracy-success?style=for-the-badge&logo=tensorflow&logoColor=white)](#-results)

<br/>

<img src="https://img.shields.io/badge/Python-3.10-3776AB?style=flat-square&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=flat-square&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Gemini%20AI-Powered-4285F4?style=flat-square&logo=google&logoColor=white"/>
<img src="https://img.shields.io/badge/License-MIT-22c55e?style=flat-square"/>
<img src="https://img.shields.io/github/last-commit/Jaskirat8904/Brain-Tumor-Prediction-?style=flat-square&color=orange"/>
<img src="https://img.shields.io/github/stars/Jaskirat8904/Brain-Tumor-Prediction-?style=flat-square&color=yellow"/>

<br/><br/>

> **NeuroVibe** is an end-to-end deep learning system that classifies brain tumors from MRI scans in under 2 seconds —
> benchmarking 5 architectures, deploying the best, and explaining every result with Gemini AI.
> Built for clinicians, researchers, and students who need answers fast.

<br/>

[**Explore the Dashboard →**](#-dashboard) · [**View Results →**](#-results-at-a-glance) · [**Quick Start →**](#-quick-start) · [**Read the Paper →**](#-citation)

---

</div>

<br/>

## 🩻 What is NeuroVibe?

Every year, **over 300,000 people** are diagnosed with brain tumors. The difference between catching a glioma early and catching it late can be the difference between life and death. Yet radiologists are overworked, MRI backlogs are growing, and small rural hospitals often lack specialist access entirely.

**NeuroVibe** is our answer.

It's a fully open-source, browser-based diagnostic aid that takes a raw MRI image and returns a tumor classification — with class probabilities, clinical guidance, and an AI-generated explanation — in under 2 seconds. No server. No installation. No cost.

Under the hood, we trained and benchmarked **five state-of-the-art CNN architectures** under strictly identical conditions to find the best model for this task. The winner, **EfficientNetB3**, achieved **93.1% test accuracy** and powers the live dashboard.

<br/>

---

## 🏆 Results at a Glance

<div align="center">

| Rank | Model | Accuracy | Parameters | Verdict |
|:---:|:---|:---:|:---:|:---|
| 🥇 | **EfficientNetB3** | **93.1%** | 12.0M | ✅ **Deployed — best accuracy** |
| 🥈 | InceptionV3 | 91.5% | 23.9M | Strong multi-scale extractor |
| 🥉 | Xception | 90.2% | 22.9M | Best depthwise separable design |
| 4 | ResNet50 | 89.4% | 25.6M | Requires BatchNorm special handling |
| 5 | MobileNetV2 | 88.7% | 3.4M | 🏅 Best efficiency — ideal for mobile |

</div>

```
Test Accuracy

EfficientNetB3  ████████████████████████████████████████████  93.1%
InceptionV3     ██████████████████████████████████████████    91.5%
Xception        █████████████████████████████████████████     90.2%
ResNet50        ████████████████████████████████████████      89.4%
MobileNetV2     ████████████████████████████████████████      88.7%
```

> All five models were trained under **100% identical conditions** — same optimizer, callbacks, classification head, and preprocessing pipeline. Performance differences are purely architectural.

<br/>

---

## 📸 Dashboard

<table>
<tr>
<td width="50%" align="center">
<img src="Screenshots/1.png" width="100%"/>
<br/><sub><b>① Home — Drag and drop MRI upload</b></sub>
</td>
<td width="50%" align="center">
<img src="Screenshots/2.png" width="100%"/>
<br/><sub><b>② Scan loaded — preview before analysis</b></sub>
</td>
</tr>
<tr>
<td width="50%" align="center">
<img src="Screenshots/3.png" width="100%"/>
<br/><sub><b>③ Prediction output with confidence score</b></sub>
</td>
<td width="50%" align="center">
<img src="Screenshots/4.png" width="100%"/>
<br/><sub><b>④ Probability bars + clinical guidance</b></sub>
</td>
</tr>
<tr>
<td width="50%" align="center">
<img src="Screenshots/5.png" width="100%"/>
<br/><sub><b>⑤ Session history — up to 25 past analyses</b></sub>
</td>
<td width="50%" align="center">
<img src="Screenshots/6.png" width="100%"/>
<br/><sub><b>⑥ Export report — .txt, clipboard, print</b></sub>
</td>
</tr>
<tr>
<td colspan="2" align="center">
<img src="Screenshots/7.png" width="50%"/>
<br/><sub><b>⑦ Research-use consent gate</b></sub>
</td>
</tr>
</table>

<br/>

---

## ✨ Dashboard Features

<table>
<tr>
<td valign="top" width="50%">

**🔬 Core Prediction Engine**
- Drag-and-drop MRI upload (PNG · JPG · WEBP · up to 20 MB)
- Real-time tumor classification in under 2 seconds
- Animated probability bars for all 4 classes
- Low-confidence alert when score falls below 70%

**🤖 AI-Powered Explanations**
- Google Gemini API generates plain-language clinical summaries
- Class-specific medical guidance and next-step recommendations
- Exportable as `.txt` report, clipboard copy, or print

</td>
<td valign="top" width="50%">

**🕓 Session and History**
- Stores up to 25 analyses per session
- Review and compare past predictions instantly

**🎨 Accessibility and UX**
- Dark / Light / High-Contrast theme modes
- Multi-language: English · Spanish · French · Arabic · Hindi
- Research-use disclaimer consent gate on first launch
- Zero installation — runs entirely in the browser

</td>
</tr>
</table>

<br/>

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    INPUT LAYER                          │
│              MRI Scan (JPG / PNG / WEBP)                │
└───────────────────────┬─────────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────────┐
│               PREPROCESSING PIPELINE                    │
│  Resize → Normalize [0,1] → Augment (train only)        │
│  Brightness ±20% · Flip · Rotation · Zoom               │
└───────────────────────┬─────────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────────┐
│            TRANSFER LEARNING BACKBONE                   │
│                                                         │
│   ImageNet Pretrained Weights (frozen)                  │
│   ┌──────────────────────────────────────────────┐      │
│   │  EfficientNetB3  ← DEPLOYED  (93.1% acc.)    │      │
│   │  InceptionV3                 (91.5% acc.)    │      │
│   │  Xception                    (90.2% acc.)    │      │
│   │  ResNet50                    (89.4% acc.)    │      │
│   │  MobileNetV2                 (88.7% acc.)    │      │
│   └──────────────────────────────────────────────┘      │
│                        │                                │
│            Global Max Pooling                           │
└───────────────────────┬─────────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────────┐
│              CUSTOM CLASSIFICATION HEAD                 │
│   (Identical across all 5 models for fair comparison)   │
│                                                         │
│   Flatten → Dropout(0.3) → Dense(128, ReLU)             │
│          → Dropout(0.25) → Dense(4, Softmax)            │
└───────────────────────┬─────────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────────┐
│                  OUTPUT (4 CLASSES)                     │
│                                                         │
│  🔴 Glioma  🟡 Meningioma  🔵 Pituitary  🟢 No Tumor   │
└─────────────────────────────────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────────┐
│              NEUROVIBE DASHBOARD                        │
│   Prediction · Confidence · Probability Bars            │
│   Gemini AI Explanation · Report Export · History       │
└─────────────────────────────────────────────────────────┘
```

<br/>

---

## 🗂️ Dataset

| Property | Details |
|:---|:---|
| **Source** | [Brain Tumor MRI Dataset — Kaggle (Nickparvar, 2021)](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) |
| **Total Images** | 7,023 labeled MRI scans |
| **Classes** | Glioma · Meningioma · Pituitary Tumor · No Tumor |
| **Training Set** | ~5,712 images |
| **Validation Set** | ~655 images (stratified split) |
| **Test Set** | ~656 images (stratified split) |
| **Splitting Strategy** | Stratified sampling · fixed `random_state=20` |
| **Format** | JPG / PNG |

<details>
<summary><b>📊 Per-class image distribution</b></summary>
<br/>

| Class | Train | Validation | Test |
|:---|:---:|:---:|:---:|
| Glioma | 1,321 | 164 | 164 |
| Meningioma | 1,339 | 165 | 165 |
| Pituitary | 1,457 | 165 | 165 |
| No Tumor | 1,595 | 163 | 163 |
| **Total** | **5,712** | **657** | **657** |

</details>

<br/>

---

## ⚙️ Technical Deep Dive

<details>
<summary><b>🔧 Training Configuration</b></summary>
<br/>

| Parameter | Value |
|:---|:---|
| Optimizer | Adamax |
| Loss Function | Categorical Cross-Entropy |
| Initial Learning Rate | 0.001 |
| Max Epochs | 10–20 |
| Batch Size | 32 |
| Base Weights | ImageNet (include_top=False) |
| Pooling | Global Max Pooling |
| EarlyStopping | patience=3 · restore best weights |
| ReduceLROnPlateau | factor=0.2 · patience=2 |
| Augmentation | Brightness [0.8, 1.2] · Flip · Rotation · Zoom |
| Tracked Metrics | Accuracy · Precision · Recall · Loss |

</details>

<details>
<summary><b>📐 Architecture-specific notes</b></summary>
<br/>

**EfficientNetB3** — Uses internal preprocessing; does **not** require external pixel rescaling. Compound scaling (depth × width × resolution) makes it the most parameter-efficient high-accuracy model in this benchmark.

**Xception** — Fully depthwise separable convolutions decouple spatial and cross-channel feature learning. Particularly effective at capturing MRI texture gradients and boundary irregularities.

**InceptionV3** — Factorized convolutions (1×n + n×1 decomposition) reduce computation while maintaining receptive field. Achieved 91.5% — strong multi-scale feature extraction on this dataset.

**MobileNetV2** — Inverted residuals with linear bottlenecks make it 6.7× lighter than Xception. At 88.7% accuracy with only 3.4M parameters, it is the clear winner for mobile or edge deployment.

**ResNet50** — BatchNormalization layers must be kept **trainable** (not frozen) during transfer learning. Frozen ImageNet statistics mismatch MRI data distributions and cause convergence failure — a known Keras transfer learning edge case.

</details>

<details>
<summary><b>📊 Evaluation metrics explained</b></summary>
<br/>

| Metric | What it tells you |
|:---|:---|
| **Accuracy** | Overall proportion of correctly classified scans |
| **Precision** | Of all scans predicted as tumor X, how many actually are |
| **Recall (Sensitivity)** | Of all actual tumor X cases, how many were caught |
| **F1-Score** | Harmonic mean of precision and recall |
| **Specificity** | How reliably the model identifies healthy scans |
| **AUC-ROC** | Overall discrimination ability across all thresholds |

> In medical imaging, **recall (sensitivity) is the critical metric.** Missing a real tumor (false negative) is far more dangerous than a false alarm.

</details>

<br/>

---

## 📁 Repository Structure

```
Brain-Tumor-Prediction-/
│
├── 📁 Screenshots/
│   ├── 1.png  →  Home / upload interface
│   ├── 2.png  →  Scan preview before analysis
│   ├── 3.png  →  Prediction + confidence output
│   ├── 4.png  →  Probability distribution + clinical guidance
│   ├── 5.png  →  Session history drawer
│   ├── 6.png  →  Export report modal
│   └── 7.png  →  Research consent gate
│
├── 🌐 app.html                          ←  NeuroVibe web dashboard
│
├── 📓 brain-tumor-xception.ipynb        ←  Xception      |  90.2% acc.
├── 📓 brain-tumor-efficientnetb3.ipynb  ←  EfficientNetB3|  93.1% acc. ✅
├── 📓 brain-tumor-inceptionv3.ipynb     ←  InceptionV3   |  91.5% acc.
├── 📓 brain-tumor-mobilenetv2.ipynb     ←  MobileNetV2   |  88.7% acc.
├── 📓 brain-tumor-resnet50.ipynb        ←  ResNet50      |  89.4% acc.
│
└── 📄 README.md
```

<br/>

---

## 🚀 Quick Start

### Option A — Just open the dashboard (zero setup)

```bash
git clone https://github.com/Jaskirat8904/Brain-Tumor-Prediction-.git
cd Brain-Tumor-Prediction-

# macOS / Linux
open app.html

# Windows
start app.html
```

> No Python. No server. No dependencies. The dashboard is a self-contained HTML file.

---

### Option B — Train or retrain the models

**Step 1 — Clone and install**

```bash
git clone https://github.com/Jaskirat8904/Brain-Tumor-Prediction-.git
cd Brain-Tumor-Prediction-
pip install -r requirements.txt
```

**Step 2 — Download the dataset from Kaggle**

Place the dataset at:
```
/kaggle/input/brain-tumor-mri-dataset/
    Training/
        glioma/ · meningioma/ · pituitary/ · notumor/
    Testing/
        glioma/ · meningioma/ · pituitary/ · notumor/
```

**Step 3 — Open a training notebook**

| Notebook | Model | Accuracy | Best for |
|:---|:---|:---:|:---|
| `brain-tumor-efficientnetb3.ipynb` | EfficientNetB3 | 93.1% | Best overall accuracy |
| `brain-tumor-inceptionv3.ipynb` | InceptionV3 | 91.5% | Multi-scale features |
| `brain-tumor-xception.ipynb` | Xception | 90.2% | Texture-heavy MRI data |
| `brain-tumor-resnet50.ipynb` | ResNet50 | 89.4% | Deep residual learning |
| `brain-tumor-mobilenetv2.ipynb` | MobileNetV2 | 88.7% | Mobile / edge deployment |

<details>
<summary><b>📦 Full requirements</b></summary>

```txt
tensorflow>=2.10
keras
numpy
pandas
matplotlib
plotly
opencv-python
scikit-learn
google-generativeai
streamlit
Pillow
```

```bash
pip install -r requirements.txt
```

</details>

<br/>

---

## 🗺️ Roadmap

| Status | Feature |
|:---:|:---|
| ✅ | 5-model benchmark under a unified, reproducible training pipeline |
| ✅ | Interactive browser dashboard with Gemini AI explanations |
| ✅ | Session history, report export, multi-language, theme modes |
| 🔄 | Grad-CAM heatmap overlay for visual explainability |
| 🔄 | DICOM (.dcm) file support for direct hospital integration |
| 🔄 | Multi-model ensemble inference in the dashboard |
| 🔄 | Expanded dataset with multi-center clinical MRI scans |
| 🔄 | Cloud deployment with EHR integration |
| 🔄 | Multilingual AI-generated PDF reports |
| 🔄 | MobileNetV2 optimized mobile inference pipeline |

<br/>

---

## 🤝 Contributing

Contributions are welcome. To get started:

1. Fork the repo
2. Create a branch: `git checkout -b feature/grad-cam-heatmaps`
3. Commit your changes: `git commit -m "Add Grad-CAM visual explainability"`
4. Push and open a Pull Request

Please open an issue first to discuss major changes.

<br/>

---

## 📚 Citation

If you use NeuroVibe in your research or coursework, please cite:

```bibtex
@misc{chopra2024neurovibe,
  author       = {Chopra, Jaskirat Singh and Kumar, Gagan},
  title        = {NeuroVibe: A Comparative Study of Deep Learning Architectures
                  for Multi-Class Brain Tumor Classification from MRI Images},
  year         = {2024},
  institution  = {Jaipur Engineering College and Research Centre},
  url          = {https://github.com/Jaskirat8904/Brain-Tumor-Prediction-}
}
```

**Key references this project builds on:**

- Tan, M. & Le, Q.V. (2019). EfficientNet: Rethinking model scaling. *ICML*. — [Paper](https://arxiv.org/abs/1905.11946)
- Chollet, F. (2017). Xception: Deep learning with depthwise separable convolutions. *IEEE CVPR*. — [Paper](https://arxiv.org/abs/1610.02357)
- Sandler, M. et al. (2018). MobileNetV2: Inverted residuals and linear bottlenecks. *IEEE CVPR*. — [Paper](https://arxiv.org/abs/1801.04381)
- Nickparvar, M. (2021). Brain Tumor MRI Dataset. *Kaggle*. — [Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)

<br/>

---

## ⚠️ Disclaimer

> **NeuroVibe is a research and educational tool only.**
>
> It is **not a certified medical device** and must **not** be used as a substitute for professional medical advice, diagnosis, or treatment. Predictions have not been validated against clinical diagnostic standards. Always consult a licensed neuroradiologist or neurosurgeon for clinical decisions.
>
> By using this software, you agree that the authors bear no liability for any medical decisions made based on its output.

<br/>

---

## 👨‍💻 Authors

<table>
<tr>
<td align="center" width="220">
<b>Jaskirat Singh Chopra</b><br/>
<sub>B.Tech CSE · JECRC Jaipur</sub><br/>
<a href="mailto:jaskiratsinghchopra.cse26@jecrc.ac.in"><sub>📧 Email</sub></a>
</td>
<td align="center" width="220">
<b>Gagan Kumar</b><br/>
<sub>B.Tech CSE · JECRC Jaipur</sub><br/>
<a href="mailto:gagankumar.cse26@jecrc.ac.in"><sub>📧 Email</sub></a>
</td>
<td align="center" width="220">
<b>Prof. Khushboo Sharma</b><br/>
<sub>Assistant Professor · CSE Dept.</sub><br/>
<a href="mailto:khushboosharma.cse@jecrc.ac.in"><sub>📧 Email</sub></a>
</td>
</tr>
</table>

**Jaipur Engineering College and Research Centre (JECRC)**
Rajasthan Technical University · Jaipur, India · 2024

<br/>

---

## 📜 License

Distributed under the [MIT License](LICENSE). Free to use, modify, and distribute with attribution.

---

<div align="center">

**If NeuroVibe helped you, please consider giving it a ⭐**

It takes 2 seconds and helps other researchers discover this project.

<br/>

[![](https://img.shields.io/badge/Made%20with-love%20%26%20caffeine-red?style=flat-square)](https://github.com/Jaskirat8904/Brain-Tumor-Prediction-)
[![](https://img.shields.io/badge/JECRC-Jaipur%2C%20India-orange?style=flat-square)](https://jecrc.ac.in)
[![](https://img.shields.io/badge/Research-Educational%20Use%20Only-blue?style=flat-square)](#️-disclaimer)

*NeuroVibe · 2024 · MIT License*

</div>
