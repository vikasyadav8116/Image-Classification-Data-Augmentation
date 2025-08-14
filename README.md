# 🖼️ Comparative Analysis of Image Classification using Data Augmentation

## 📌 Overview
This project compares multiple **image processing strategies** for CNN-based image classification using the **NIH Malaria Dataset** (~2.7M images).  
We implemented and tested four strategies on the same LeNet-5 architecture to evaluate their impact on accuracy and generalization.

**Strategies Tested:**
1. **Baseline Model** – LeNet-5 without augmentation.
2. **Mixup Augmentation** – Blends pairs of images and their labels.
3. **CutMix Augmentation** – Replaces image regions with patches from other images.
4. **Combined Augmentation** – Resizing, flipping, rotation, contrast adjustment, normalization.

---

## 🛠️ Tech Stack
- **Languages & Libraries:** Python, TensorFlow, OpenCV, Albumentations
- **Environment:** Google Colab
- **Dataset:** [NIH Malaria Dataset](https://ceb.nlm.nih.gov/repositories/malaria-datasets/)

---

## 📂 Dataset Description
- Total Images: ~2.7M
- Classes: `Infected` vs `Uninfected`
- Images resized and preprocessed for CNN input.
- Pixel-level differences indicate presence of malaria parasites.

---

## ⚙️ How It Works
- **Architecture:** LeNet-5 (Convolutional layers + BatchNorm + MaxPooling + Dense layers)
- **Training:** 20 epochs, same hyperparameters for all strategies
- **Evaluation Metrics:** Accuracy, Loss (Training & Validation)

---

## 📊 Results

| Strategy  | Accuracy | Loss   | Val Accuracy | Val Loss |
|-----------|----------|--------|--------------|----------|
| Baseline  | 94.4%    | 0.1442 | 93.9%        | 0.1820   |
| Mixup     | 48.3%    | 0.2805 | 39.8%        | 0.2468   |
| CutMix    | 49.1%    | 0.2225 | 37.8%        | 0.3088   |
| Combined  | **95.4%**| 0.1645 | 89.8%        | 0.2122   |

**Conclusion:**  
The **Combined Augmentation** strategy achieved the best overall accuracy and robustness, outperforming both Mixup and CutMix individually.

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/YourUsername/Image-Classification-Data-Augmentation.git
cd Image-Classification-Data-Augmentation

# Install dependencies
pip install -r requirements.txt

# Run the training script
python train.py
```

---

## 📌 Future Scope
- Experiment with advanced augmentation (e.g., GAN-based synthetic data).
- Apply findings to other medical datasets for generalization testing.
- Optimize Mixup and CutMix parameters for improved results.

---

## 👤 Author
**Vikas Yadav**  
B.Tech, Computer Science Engineering – KIIT University  
📧 Email: vikasyadav8116@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/vikasyadav) | [GitHub](https://github.com/vikasyadav8116)
