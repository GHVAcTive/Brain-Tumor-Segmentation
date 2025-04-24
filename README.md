# 🧠 Brain Tumor Segmentation using Deep Learning  
## Multi-Technique Comparison for MRI Segmentation

![Sample Segmentation Placeholder](https://via.placeholder.com/600x200.png?text=Sample+Segmentation+Result)  
*Replace with an actual image from your results (e.g., Imgur or local upload)*

-----

## 🎯 Problem Statement

Brain tumor segmentation in Magnetic Resonance Imaging (MRI) scans is a critical first step for **diagnosis, treatment planning, surgical guidance, and monitoring disease progression**. However, manual segmentation by expert radiologists is:

- Laborious and time-consuming ⏱️  
- Prone to inter-observer variability ⚠️  

This project automates the segmentation process using **three deep learning techniques** on 3D MRI volumes. It addresses key challenges such as:

- 🎲 **Variable tumor shapes, sizes, and locations**  
- ⚖️ **Significant class imbalance** (tumors are typically small compared to the brain volume)  
- 🧊 **Preserving 3D spatial context** for accurate analysis  
- 💡 **Using accessible, synthetic data** to ensure reproducibility

---

## 🛠️ Project Explanation

The repository includes a Jupyter Notebook implementation comparing **three architectures** for brain tumor segmentation:

### 📌 Models Compared:

1. **U-Net (Baseline):**  
   A widely used encoder-decoder model in biomedical imaging. Uses skip connections for better feature propagation.

2. **Attention U-Net:**  
   Enhances U-Net with **Attention Gates** to suppress irrelevant features and focus on tumor-specific regions.

3. **Transformer-Enhanced Model:**  
   Combines **CNNs and Transformers**—local features are extracted using CNNs and long-range dependencies are captured via Transformer blocks.

---

### ✨ Key Features:

- Multi-model comparison: U-Net, Attention U-Net, Transformer Hybrid  
- Synthetic 3D MRI data generation: `128x128x128` volumes  
- Attention integration in U-Net  
- Basic Transformer block fusion  
- Evaluation metrics: **Dice Score**, **Mean IoU**  
- Clear training visualizations and segmentation results

> ⚠️ **Note:** Although this project processes 3D data, models currently use `Conv2D` layers for simplicity. For real-world performance, migrate to `Conv3D`, `MaxPooling3D`, etc.

---

## 💾 Dataset

This project uses **synthetic 3D MRI data** generated within the notebook (`load_sample_data` function).

### 🧪 Synthetic Data Features:
- Size: `128x128x128`  
- Random noise background  
- Simulated spherical tumors with high intensity

### 📚 For Real-World Use:
Use the **BraTS Challenge Dataset**, hosted in datasets like:
- [Medical Segmentation Decathlon – Task 1: Brain Tumour](http://medicaldecathlon.com/)

> Note: Requires registration. Preprocessing real-world data often includes format conversion (e.g., using `nibabel`) and normalization pipelines.

---

## ⚙️ Installation

```bash
# Clone the repository
# git clone https://github.com/yourusername/brain-tumor-segmentation.git
# cd brain-tumor-segmentation

# Install dependencies
pip install tensorflow numpy matplotlib scikit-learn

# Optional: For working with BraTS or NIfTI data
pip install nibabel
```

---

## ▶️ Usage

1. Ensure dependencies are installed  
2. Open the notebook:

```bash
jupyter notebook Brain_Tumor_Segmentation.ipynb
```

3. Run all cells sequentially:

- Generate synthetic data  
- Build and train models  
- Evaluate and visualize results

---

## 📊 Results

> *(Replace these with your actual results)*

| Model                | Validation Dice Score | Validation IoU | Inference Time (per volume) |
|----------------------|-----------------------|----------------|-----------------------------|
| U-Net                | 0.82                  | 0.75           | ~12s                        |
| Attention U-Net      | 0.85                  | 0.77           | ~14s                        |
| Transformer-Enhanced | 0.83                  | 0.76           | ~18s                        |

### Sample Comparison

*Replace with actual side-by-side output image from your notebook.*

---

## 👋 Contributing

Contributions, issues, and feature requests are welcome!

- Open an issue first to discuss any proposed changes  
- Feel free to fork, improve, and send pull requests 🚀

---

## 📜 License

Distributed under the **MIT License**.  
See the `LICENSE` file for details.

---

## 📚 Sources & References

1. https://github.com/kiptubei/PetCity  
2. [U-Net Paper (Ronneberger et al., 2015)](https://arxiv.org/abs/1505.04597)  
3. [Attention U-Net (Oktay et al., 2018)](https://arxiv.org/abs/1804.03999)  
4. [TransUNet (Chen et al., 2021)](https://arxiv.org/abs/2102.04306)  

---

Let me know if you want this exported to a `.md` file or tailored to a specific format like a GitHub Pages site or presentation deck!
