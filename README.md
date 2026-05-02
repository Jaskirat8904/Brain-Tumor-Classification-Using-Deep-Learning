# 🧠 Brain Tumor Classification from MRI Scans Using Deep Learning

> **NeuroVibe** — An intelligent multi-model deep learning system for automated brain tumor detection, classification, and AI-powered clinical explanation.

![GitHub repo size](https://img.shields.io/github/repo-size/Jaskirat8904/Brain-Tumor-Prediction-)
![GitHub last commit](https://img.shields.io/github/last-commit/Jaskirat8904/Brain-Tumor-Prediction-)
![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Project Overview

This project develops an automated brain tumor classification system using transfer learning and pretrained CNN architectures. MRI scan images are classified into four categories: **Glioma**, **Meningioma**, **Pituitary Tumor**, and **No Tumor**. The system benchmarks five deep learning models under a unified training configuration and deploys the results through an interactive dashboard with Gemini AI-powered explanations.

---

## 🎯 Objectives

- Automate brain tumor detection and classification from MRI images
- Benchmark five pretrained CNN architectures under identical training conditions
- Identify the most accurate and efficient model for deployment
- Provide an interactive dashboard for real-time MRI scan classification
- Generate AI-powered clinical explanations using the Gemini API

---

## 📸 Screenshots

### 🏠 Home Page — Upload Interface
![Home Page](Screenshots/1.png)

### 📤 MRI Scan Uploaded — Ready to Analyze
![Upload Preview](Screenshots/2.png)

### 🔬 Analysis Results — Prediction & Confidence
![Analysis Results](Screenshots/3.png)

### 📊 Probability Distribution & Clinical Recommendation
![Probability Distribution](Screenshots/4.png)

### 🕓 Session History Drawer
![Session History](Screenshots/5.png)

### 📄 Export Report Modal
![Export Report](Screenshots/6.png)

### 🛡️ Research Use Only — Consent Gate
![Consent Gate](Screenshots/7.png)

---

## 🗂️ Dataset

| Property       | Details                              |
|----------------|--------------------------------------|
| Source         | Figshare Brain MRI Dataset (Kaggle)  |
| Total Images   | 7,023 labeled MRI scans              |
| Classes        | Glioma, Meningioma, Pituitary, No Tumor |
| Split          | 80% Train / 10% Validation / 10% Test |
| Format         | JPG / PNG images                     |

---

## 🏗️ Project Structure

```
Brain-Tumor-Prediction-/
│
├── Screenshots/
│   ├── 1.png
│   ├── 2.png
│   ├── 3.png
│   ├── 4.png
│   ├── 5.png
│   ├── 6.png
│   └── 7.png
│
├── app.html                          ← NeuroVibe Web Dashboard
│
├── brain-tumor-xception.ipynb
├── brain-tumor-efficientnetb3.ipynb
├── brain-tumor-inceptionv3.ipynb
├── brain-tumor-mobilenetv2.ipynb
├── brain-tumor-resnet50.ipynb
│
└── README.md
```

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Images resized to **224 × 224 pixels**
- Pixel values normalized to [0, 1] range
- Stratified train/validation/test split applied

### 2. Data Augmentation
- Random horizontal flipping
- Rotation and zoom
- Brightness adjustment
- Applied only to training set to prevent data leakage

### 3. Models Used

| Model          | Parameters | Architecture Highlight               |
|----------------|------------|---------------------------------------|
| Xception       | ~22M       | Depthwise separable convolutions      |
| MobileNetV2    | ~3.5M      | Inverted residuals, lightweight       |
| InceptionV3    | ~23M       | Multi-scale parallel branches         |
| EfficientNetB3 | ~12M       | Compound scaling (depth/width/res)    |
| ResNet50       | ~25M       | Residual skip connections             |

### 4. Training Configuration

| Parameter        | Value                         |
|------------------|-------------------------------|
| Optimizer        | Adam                          |
| Loss Function    | Categorical Cross-Entropy     |
| Learning Rate    | 0.0001                        |
| Epochs           | 20                            |
| Input Size       | 224 × 224 × 3                 |
| Batch Size       | 32                            |
| Transfer Learning| ImageNet pretrained weights   |

---

## 📊 Results

| Model              | Test Accuracy |
|--------------------|---------------|
| Xception           | 90.2%         |
| MobileNetV2        | 88.7%         |
| InceptionV3        | 91.5%         |
| **EfficientNetB3** | **93.1% ✅**  |
| ResNet50           | 89.4%         |

> ✅ **EfficientNetB3 achieved the highest accuracy of 93.1%** and was selected as the final model for deployment.

---

## 📐 Evaluation Metrics

| Metric        | Description                                      |
|---------------|--------------------------------------------------|
| Accuracy      | Overall correct predictions                      |
| Precision     | True positives out of all predicted positives    |
| Recall        | True positives out of all actual positives       |
| F1 Score      | Harmonic mean of precision and recall            |
| Specificity   | True negatives out of all actual negatives       |
| AUC-ROC       | Area under the ROC curve                         |

---

## 🖥️ Dashboard Features

- **Drag-and-drop MRI upload** — PNG, JPG, WEBP up to 20 MB
- **Real-time prediction** — Instant tumor class output with confidence score
- **Probability distribution** — Animated bars for all four classes
- **Low-confidence warning** — Alert when score falls below 70%
- **Clinical recommendations** — Class-specific medical guidance
- **Session history** — Stores up to 25 past analyses
- **AI explanation** — Gemini API generates readable clinical descriptions
- **Report export** — Downloadable `.txt`, clipboard copy, and print support
- **Theme modes** — Dark, Light, and High-Contrast
- **Multi-language support** — English, Spanish, French, Arabic, Hindi

---

## 🛠️ Tech Stack

| Component         | Technology                        |
|-------------------|-----------------------------------|
| Language          | Python                            |
| Deep Learning     | TensorFlow / Keras                |
| Preprocessing     | OpenCV, NumPy, Pandas             |
| Visualization     | Plotly, Matplotlib                |
| Dashboard         | HTML + Tailwind CSS + JavaScript  |
| AI Explanation    | Google Gemini API                 |
| Development Env   | Kaggle Notebooks / Google Colab   |

---

## 📦 Requirements

```
tensorflow>=2.10
keras
numpy
pandas
matplotlib
plotly
streamlit
opencv-python
scikit-learn
google-generativeai
```

Install all dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/Jaskirat8904/Brain-Tumor-Prediction-.git
cd Brain-Tumor-Prediction-
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run model training notebooks
Open any of the `.ipynb` notebooks in Kaggle or Jupyter:
```
brain-tumor-xception.ipynb
brain-tumor-efficientnetb3.ipynb
brain-tumor-inceptionv3.ipynb
brain-tumor-mobilenetv2.ipynb
brain-tumor-resnet50.ipynb
```

### 4. Launch the dashboard
Simply open `app.html` in your browser.

---

## ⚠️ Limitations

- Supports only JPG/PNG/WEBP formats — **no DICOM support**
- Trained on a single dataset which may not generalize across all MRI scanners
- Currently deploys one model at a time in the live dashboard
- Not intended for clinical use — **research and educational purposes only**

---

## 🔮 Future Scope

- Add **DICOM file support** for direct hospital integration
- Integrate **Grad-CAM heatmaps** for visual explainability
- Support **multi-model ensemble inference** in the dashboard
- Expand dataset with multi-center clinical MRI scans
- Deploy as a **cloud-based clinical decision support tool** with EHR integration
- Add **multilingual AI-generated reports** using advanced language models

---

## ⚠️ Disclaimer

> This project is developed for **research and educational purposes only**. It is **not a certified medical device** and must not be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified neuroradiologist or neurosurgeon for clinical decisions.

---

## 👨‍💻 Author

**Jaskirat Singh**
B.Tech Computer Science Engineering
Rajasthan Technical University, Jaipur

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
