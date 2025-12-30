# 🧠 DermalScan: AI_Facial Skin Detection App

## 📌 Project Overview
This project focuses on analyzing facial skin conditions from images using deep learning and computer vision techniques.  
The system detects faces and classifies facial skin into four categories:

- Wrinkles  
- Dark Spots  
- Puffy Eyes  
- Clear Skin  

The project follows a **milestone-based development approach**, covering dataset creation, preprocessing, model training, face detection, and deployment through a web interface.

---

## 🎯 Objectives
- Create a custom facial skin dataset using web scraping.
- Clean, label, and balance the dataset for reliable training.
- Preprocess and augment images for deep learning models.
- Train a CNN using transfer learning.
- Build a face detection and prediction pipeline.
- Develop an end-to-end web application for inference and result export.

---

## 🗂️ Project Milestones & Modules

### 🔹 Milestone 1: Dataset Preparation and Preprocessing

#### Module 1: Dataset Setup and Image Labeling
- Custom dataset created by **web scraping publicly available facial images**.
- Images manually inspected, cleaned, and labeled.
- Four skin condition classes defined.
- Class distribution balanced to reduce bias.

#### Module 2: Image Preprocessing and Augmentation
- Images resized to **224 × 224**.
- Pixel normalization and label encoding applied.
- Data augmentation techniques:
  - Horizontal flip
  - Rotation
  - Zoom
- Augmentation visualizations generated to verify data quality.

---

### 🔹 Milestone 2: Model Training and Evaluation

#### Module 3: Model Training with EfficientNetB0
- Used **EfficientNetB0** pretrained on ImageNet for transfer learning.
- Loss function: Categorical Cross-Entropy.
- Optimizer: Adam.
- Training and validation accuracy and loss monitored using plots.

#### Module 4: Face Detection and Prediction Pipeline
- Face detection implemented using **OpenCV Haar Cascade**.
- Detected face regions cropped and preprocessed before prediction.
- Trained CNN used to classify facial skin conditions.
- Predictions displayed as class labels with confidence scores.

> **Note:** MediaPipe Face Detection was explored and tested during development as a fallback approach.  
> It was not included in the final deployed application due to **library compatibility constraints** in the target environment.  
> To ensure stability and reproducibility, the final system relies solely on Haar Cascade.

---

### 🔹 Milestone 3: Frontend and Backend Integration

#### Modules 5, 6 & 7: Web UI, Backend Inference, and Export
- User interface developed using **Streamlit**.
- Image upload and preview functionality implemented.
- Backend inference pipeline integrated with the trained model.
- Prediction results displayed with bounding boxes and probabilities.
- Export features:
  - Download annotated images
  - Export prediction results as CSV
- Prediction logs maintained for analysis.

These modules are combined to form a **seamless end-to-end pipeline**.

---

### 🔹 Milestone 4: Finalization and Delivery

#### Module 8: Documentation and Final Presentation
- Prepared final project documentation and presentation slides.
- Documented methodology, architecture, results, challenges, and future scope.

---

## 🧩 System Architecture

```text
User Uploads Image
        │
        ▼
Face Detection Module
(OpenCV Haar Cascade)
        │
        ▼
Face Cropping & Preprocessing
(Resize 224×224, Normalization)
        │
        ▼
EfficientNetB0 CNN Model
        │
        ▼
Skin Condition Prediction
(Class + Confidence Score)
        │
        ▼
Web Interface Visualization
+ Export (CSV / Annotated Image)
```
## 🛠️ Technologies Used
- **Python** – Core programming language  
- **TensorFlow / Keras** – Deep learning framework for model training  
- **EfficientNetB0** – Pretrained CNN model for transfer learning  
- **OpenCV** – Face detection and image processing  
- **Streamlit** – Web interface for image upload and result visualization  
- **NumPy** – Numerical computations  
- **Matplotlib** – Data and result visualization  

---

## 📁 Dataset Information
- The dataset was **custom-created using web scraping** from publicly available sources.
- Facial images were manually inspected, cleaned, and labeled.
- Four facial skin condition classes were defined:
  - Wrinkles  
  - Dark Spots  
  - Puffy Eyes  
  - Clear Skin  
- Class distribution was balanced to reduce bias during training.
- The dataset is **not included in the repository** due to size constraints.
- Dataset structure and sample visualizations are provided for reference.

---

## ⚠️ Limitations
- Haar Cascade face detection may struggle under extreme lighting conditions or non-frontal face poses.
- Model performance depends on the quality and diversity of the scraped dataset.
- The system currently supports **image-based analysis only** (no real-time video processing).
- Deployment constraints limited the use of alternative face detection frameworks.

---

## 🚀 Future Scope
- Integration of real-time webcam-based facial skin analysis.
- Expansion to additional skin conditions and finer-grained classification.
- Optimization of the model for faster inference and deployment.
- Integration with a full-stack web application for broader accessibility.

---

## ✅ Conclusion
This project presents an end-to-end deep learning solution for facial skin condition analysis, covering dataset creation, preprocessing, model training, and deployment.  
It demonstrates practical application of computer vision and transfer learning while addressing real-world challenges such as data quality, robustness, and deployment constraints.

---
- 🔗 **Live Application:** https://dermaai-fhyknap4uo3l6bluyb2vki.streamlit.app/ 
- 📂 **GitHub Repository:** https://github.com/anu04596/DermaAI

