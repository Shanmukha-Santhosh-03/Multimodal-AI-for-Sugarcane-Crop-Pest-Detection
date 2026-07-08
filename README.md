# 🌱 Multimodal AI for Sugarcane Crop Disease & Insect Detection

> An AI-powered multimodal crop health diagnosis system that combines **YOLOv8 object detection** with **TabNet structured-data classification** to identify sugarcane diseases and insect infestations, improving diagnostic accuracy through prediction fusion.

---

## 📖 Overview

Early detection of crop diseases and insect infestations is essential for improving agricultural productivity and reducing economic losses. Traditional manual diagnosis is time-consuming and requires domain expertise.

This project introduces a **multimodal AI framework** that integrates:

- **YOLOv8** for image-based disease and insect detection.
- **TabNet** for questionnaire-based classification using structured agricultural data.
- **Prediction Fusion** to combine outputs from both models and generate a more reliable diagnosis.
- **Flask** web application for an easy-to-use prediction interface.

The system demonstrates how combining computer vision and tabular machine learning can improve agricultural decision support systems.

---

# ✨ Features

- 🌿 Sugarcane disease detection using YOLOv8
- 🐛 Sugarcane insect detection using YOLOv8
- 📋 Questionnaire-based prediction using TabNet
- 🤝 Fusion of image and questionnaire predictions
- 🌐 Flask-based web interface
- ⚡ Real-time inference
- 📦 Modular project architecture
- 🔍 Easy integration of new disease classes or trained models

---

# 🏗 System Architecture

```text
                Input Image
                     │
                     ▼
          YOLOv8 Disease/Insect Detection
                     │
                     ▼
          Image Prediction Results
                     │
                     │
Questionnaire --------------------------► TabNet Prediction
                     │
                     ▼
              Prediction Fusion
                     │
                     ▼
            Final Diagnosis Result
```

---

# 🛠 Technology Stack

| Category | Technology |
|-----------|------------|
| Programming Language | Python |
| Backend | Flask |
| Computer Vision | OpenCV |
| Deep Learning | PyTorch |
| Object Detection | YOLOv8 |
| Tabular Learning | TabNet |
| Data Processing | Pandas |
| Numerical Computing | NumPy |
| Dataset Annotation | CVAT |
| Frontend | HTML, CSS, JavaScript |

---

# 📂 Project Structure

```text
.
├── app.py                          # Flask application
├── detect_disease.py               # Disease detection pipeline
├── detect_insect.py                # Insect detection pipeline
├── fusion.py                       # Prediction fusion logic
├── model_handler.py                # Model loading and management
├── requirements.txt                # Project dependencies
│
├── models/
│   ├── yolov8_disease_detection.pt
│   ├── yolov8s_insect_detection_best.pt
│   ├── tabnet_disease_model.zip
│   └── tabnet_insect_model.zip
│
├── tabnet/
│   ├── predict_disease_tabnet.py
│   ├── predict_insect_tabnet.py
│   ├── prepare_round2_tabnet.py
│   └── optimize_tabnet_models.py
│
├── YOLOv8s/
│   └── train_yolov8s_insect.py
│
├── YOLOv8s-seg/
│   └── YOLOSEG.py
│
├── templates/
│   └── index.html
│
├── static/
│   ├── styles.css
│   ├── script.js
│   └── images
│
└── datasets/
```

---

# 🚀 Installation

## Clone Repository

```bash
git clone https://github.com/Shanmukha-Santhosh-03/Multimodal-AI-for-Sugarcane-Crop-Pest-Detection.git

cd Multimodal-AI-for-Sugarcane-Crop-Pest-Detection
```

---

## Create Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Application

```bash
python app.py
```

Open your browser and navigate to:

```
http://127.0.0.1:5000
```

---

# 🧠 Model Pipeline

### Image Branch

- Upload crop image
- YOLOv8 detects disease/insect
- Bounding boxes generated
- Confidence score calculated

### Structured Data Branch

- User answers questionnaire
- Features processed
- TabNet predicts probable condition

### Fusion

- Both predictions are combined
- Final diagnosis is generated

---

# 📊 Models Used

## YOLOv8

Purpose:

- Disease Detection
- Insect Detection

Framework:

- Ultralytics YOLOv8

Output:

- Bounding Boxes
- Class Labels
- Confidence Scores

---

## TabNet

Purpose:

- Structured questionnaire classification

Advantages:

- Handles tabular agricultural data
- Interpretable feature learning
- High performance on structured datasets

---

# 📁 Datasets

This project uses:

- Sugarcane disease images
- Sugarcane insect images
- Questionnaire-based agricultural datasets

Structured datasets included:

- sugarcane_deadheart_data_r2.csv
- sugarcane_insect_data_r2.csv

Image datasets were annotated using **CVAT** before training.

---

# 📈 Future Improvements

- Deploy using Docker
- Cloud deployment (AWS / Azure / GCP)
- Mobile application
- Explainable AI (Grad-CAM)
- Automatic treatment recommendation
- Multi-language support
- Disease severity estimation
- Farmer advisory dashboard

---

# 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature-name
```

3. Commit your changes

```bash
git commit -m "Add feature"
```

4. Push

```bash
git push origin feature-name
```

5. Open a Pull Request

---

# 📜 License

This project is released under the MIT License.

---

# 👨‍💻 Author

**K. Shanmukha Santhosh**

Artificial Intelligence & Machine Learning

Vellore Institute of Technology

GitHub:
https://github.com/Shanmukha-Santhosh-03

---

# ⭐ Support

If you found this project useful,

⭐ Star this repository

🍴 Fork it
