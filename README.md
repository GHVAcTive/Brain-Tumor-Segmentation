# Brain Tumor Segmentation using Deep Learning 🧠
## Multi-Technique Comparison for MRI Segmentation

![Sample Segmentation Placeholder](https://via.placeholder.com/600x200.png?text=Sample+Segmentation+Result)
*(Replace with an actual image URL from your results, e.g., using Imgur)*

---

## 🎯 Problem Statement

Brain tumor segmentation in Magnetic Resonance Imaging (MRI) scans is a critical first step for **diagnosis, treatment planning, surgical guidance, and monitoring disease progression**. However, manual segmentation by expert radiologists is laborious, time-consuming, and prone to inter-observer variability.

This project aims to automate this process by implementing and comparing **three distinct deep learning approaches** for segmenting tumors in 3D MRI volumes. The goal is to address key challenges including:

* Variable tumor shapes, sizes, and locations 🎲
* Significant class imbalance (tumors often occupy a small portion of the brain volume)⚖️
* Preserving 3D spatial context for accurate volumetric analysis 🧊
* Demonstrating model performance using accessible synthetic data 💡

---

## 🛠️ Project Explanation

This repository provides a Jupyter Notebook implementation comparing three different deep learning architectures for 3D brain tumor segmentation:

1.  **U-Net (Baseline):** The classic encoder-decoder CNN architecture, renowned for its effectiveness in biomedical image segmentation due to skip connections that combine deep, semantic features with shallow, high-resolution features.
2.  **Attention U-Net:** An enhanced U-Net incorporating 'Attention Gates'. These gates learn to suppress irrelevant regions in input features while highlighting salient features useful for the specific task, improving focus on the tumor region.
3.  **Transformer-Enhanced Model:** A hybrid architecture leveraging the strengths of both CNNs and Transformers. A CNN encoder extracts local features, which are then processed by a Transformer block to capture long-range dependencies and global context before a final CNN decoder generates the segmentation map.

**Key Features ✨:**

* Comparison of multiple advanced segmentation architectures (U-Net, Attention U-Net, Transformer Hybrid)
* Self-contained synthetic 3D MRI data generation (`128x128x128`) for easy experimentation
* Implementation of Attention mechanisms within the U-Net framework
* Integration of a basic Transformer block with a CNN backbone
* Comprehensive evaluation using standard segmentation metrics (Dice Score, Mean Intersection over Union - IoU) 📈
* Clear visualization of segmentation results and training progress 📊

**⚠️ Implementation Note:** While the project generates and processes 3D volumetric data, the current neural network implementations primarily utilize **2D convolutional layers (`Conv2D`, `MaxPooling2D`)** for simplicity and demonstration purposes. For optimal performance on real-world 3D MRI data, adapting these models to use their 3D counterparts (`Conv3D`, `MaxPooling3D`, etc.) is recommended as a next step.

---

## 💾 Dataset

This project uses **synthetically generated 3D MRI data** created programmatically within the Jupyter Notebook (`load_sample_data` function). This allows for immediate execution and experimentation without needing large external downloads.

* **Synthetic Data Characteristics:** 3D volumes (`128x128x128`), random noise background, simulated spherical tumors with higher intensity. The synthetic data aims to mimic some basic characteristics for testing the segmentation algorithms.

**For Real-World Application:**

A standard benchmark dataset for this task is the **BraTS (Brain Tumor Segmentation) Challenge dataset**.
* You can find versions of it hosted in various places, including as part of the [Medical Segmentation Decathlon](http://medicaldecathlon.com/) (Task 1: Brain Tumour).
* *Note: Access typically requires registration, and processing real BraTS data often involves additional steps like format conversion (e.g., using Nibabel) and specific preprocessing pipelines.*

---

## ⚙️ Installation

```bash
# 1. Clone the repository (replace with your actual URL if using Git)
# git clone [https://github.com/yourusername/brain-tumor-segmentation.git](https://github.com/yourusername/brain-tumor-segmentation.git)
# cd brain-tumor-segmentation

# 2. Ensure you have Python 3.8+ installed

# 3. Install required libraries 📦
pip install tensorflow numpy matplotlib scikit-learn

# Optional: For processing real NIfTI files (.nii.gz) like BraTS
# pip install nibabel


▶️ Usage
Ensure all dependencies from the Installation step are met.
Launch Jupyter Notebook:
Bash
jupyter notebook Brain_Tumor_Segmentation.ipynb
(Replace Brain_Tumor_Segmentation.ipynb if your notebook file has a different name)
Open the notebook in your browser.
Execute the cells sequentially from top to bottom. This will:
Generate the synthetic dataset.
Define the U-Net, Attention U-Net, and Transformer models.
Compile and train each model.
Evaluate the models and display performance metrics.
Visualize segmentation results and training curves.
📊 Results
(Note: The following results are illustrative placeholders based on the example provided. Replace them with the actual results obtained from running your notebook.)
Model
Validation Dice Score
Validation IoU
Est. Inference Time
U-Net
0.82
0.75
~12s / volume
Attention U-Net
0.85
0.77
~14s / volume
Transformer-Enhanced
0.83
0.76
~18s / volume

Sample Segmentation Comparison:

(Replace with an actual image URL showing side-by-side comparisons from your results)
👋 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page1 (replace with your actual repo link if applicable). Please open an issue first to discuss what you would like to change.
📜 License
Distributed under the MIT License. See LICENSE file for more information (if you have one).
MIT License



**Remember to:**

1.  Replace the placeholder image URLs with actual URLs of screenshots from your notebook's output (upload them to a service like Imgur or include them in your repository).
2.  Update the placeholder performance values in the Results table with the actual Dice scores, IoU scores, and potentially inference times you observed.
3.  If you host this project on GitHub (or elsewhere), replace placeholder URLs like `https://github.com/yourusername/brain-tumor-segmentation.git` with your actual repository URL.
4.  Create a `LICENSE` file (e.g., containing the MIT License text) if you want to formally include one.


Sources
1. https://github.com/kiptubei/PetCity
