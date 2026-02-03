# food101-resnet18-finetuning
Research-style project fine-tuning a pretrained ResNet-18 on the Food-101 dataset using selective freezing, MixUp, label smoothing, cosine LR scheduling, mixed precision, and gradient clipping, achieving 78.5% top-1 validation accuracy.


# Food-101 Image Classification with Efficient Fine-Tuning

This repository presents a deep learning study on **food image classification** using the **Food-101 dataset**, focusing on **efficient fine-tuning strategies** under realistic compute constraints (Google Colab GPU sessions).

The project was completed as part of an **8-month AEC (ACS) in Business Intelligence & Data Visualization (Data Science)** and follows a **research-style methodology** inspired by academic ML workflows.

---

## 📌 Project Objectives

- Build a **robust food image classifier** using a pretrained CNN
- Optimize performance while respecting **limited compute resources**
- Analyze the impact of **selective layer freezing** and modern regularization techniques
- Identify common **failure modes** in food image classification

---

## 🧠 Model & Approach

- **Backbone:** ResNet-18 (pretrained on ImageNet)
- **Framework:** PyTorch
- **Training Strategy:**
  - Freeze early convolutional layers
  - Fine-tune higher residual blocks (layers 2–4)
  - Lightweight classification head

---

## ⚙️ Training Techniques Used

- Transfer learning & selective freezing
- **MixUp** data augmentation
- **Label smoothing**
- **Cosine learning rate scheduling**
- **Automatic Mixed Precision (AMP)**
- **Gradient clipping**
- Two-phase resolution strategy:
  - Training at **192×192**
  - Optional final fine-tuning (“polish”) at **224×224**

---

## 📊 Results

| Resolution | Top-1 Validation Accuracy |
|----------|---------------------------|
| 192×192  | 77.1% |
| 224×224  | **78.5%** |

The resolution “polish” phase yielded a measurable performance improvement with minimal additional compute cost.

---

## 🔍 Error Analysis

Common failure cases include:
- Visually similar dishes (e.g., steak vs filet mignon)
- Occlusions and partial views
- Background bias (plates, lighting, context)

These findings highlight the importance of **data diversity** and **robust augmentation strategies**.

---

## 📄 Report

📘 **Full research report (PDF):**  
👉 *PDF file located in this repository*

The report details methodology, experiments, ablation studies, and analysis in an academic-style format.

---

## 🧰 Tools & Technologies

- Python
- PyTorch
- torchvision
- NumPy, Pandas
- Matplotlib / Seaborn
- Google Colab (GPU)
- Food-101 dataset

---

## 🚀 Future Improvements

- Try larger architectures (ResNet-34 / EfficientNet)
- Class-aware augmentation for visually similar foods
- Background debiasing techniques
- Dataset expansion or curriculum learning

---

## 👤 Author

**Mario Escalante-Contreras**  
Business Intelligence & Data Science  
📍 Montréal, Canada  

Feel free to connect or reach out via LinkedIn.
