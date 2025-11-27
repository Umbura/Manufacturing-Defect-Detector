<div align="center">

# Manufacturing Defect Detection with PaDiM

### Automated Quality Control

<!-- LANGUAGE SWITCHER -->
[![Read in Portuguese](https://img.shields.io/badge/Read%20in-Portuguese-2ea44f?style=for-the-badge&logo=google-translate&logoColor=white)](README_PT.md)

<!-- TECH STACK BADGES -->
<p>
  <img src="https://img.shields.io/badge/Python-3.9%2B-blue" alt="Python 3.9+">
  <img src="https://img.shields.io/badge/TensorFlow-2.15-orange" alt="TensorFlow 2.15">
  <img src="https://img.shields.io/badge/Accuracy-98%25-green" alt="Accuracy 98%">
</p>

<!-- MAIN IMAGE -->
<img src="https://i.imgur.com/0KGYw4w.gif" alt="PaDiM Demo" width="100%">

*Model demonstration identifying non-standard bottles (defects).*

</div>

---

## About
This project was developed for academic and educational purposes, aiming to reproduce and apply the methodology proposed in the paper **“PaDiM: a Patch Distribution Modeling Framework for Anomaly Detection and Localization”** (Defard et al., 2020).

The main objective is to explore the PaDiM methodology in the context of industrial visual inspection, applying it to the detection of manufacturing defects.

The approach is based on **one-class learning**, where the model is trained exclusively with images of "perfect" products. This makes it ideal for industrial scenarios where defects are rare and can take unpredictable forms.

The process consists of:
1.  Using a CNN (**ResNet50**) to learn deep visual features of a standard product.
2.  Statistically modeling this "normality" for each part of the product.
3.  During inspection, comparing a new product with the learned statistical model and calculating an **anomaly score**. High scores indicate a defective product.

This repository contains the complete implementation in Python, TensorFlow, and Keras, from pre-processing to final evaluation.

---

## Results

The optimized implementation achieved exceptional performance in detecting defective bottles, validating the method's effectiveness.

*   **AUC-ROC:** **0.9968**
*   **Accuracy (with optimized threshold):** **98%**

<div align="center">
  <img src="https://i.imgur.com/0KGYw4w.gif" alt="Detection Samples" width="80%">
  <p><em>Visualization of heatmaps indicating the exact location of anomalies.</em></p>
</div>

---

## Technologies Used

*   **Language:** Python 3.9+
*   **Machine Learning Frameworks:** TensorFlow, Keras, Scikit-learn
*   **Processing Libraries:** NumPy, SciPy, OpenCV
*   **Visualization:** Matplotlib, Seaborn

---

## How to Run

### Prerequisites
*   Python 3.9 or higher.
*   **MVTec AD** Dataset (specifically the "bottle" category).

### Installation and Execution
1.  **Clone this repository:**
    ```bash
    git clone https://github.com/Umbura/Manufacturing-Defect-Detector.git
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the Notebook:**
    Open and run the `main.ipynb` file.

---

## Credits and References

This project is an implementation of the original academic work by the authors of PaDiM.

*   **Scientific Paper:** Defard, T., et al. (2020). *PaDiM: A Patch Distribution Modeling Framework for Anomaly Detection and Localization*. [arXiv:2011.08785](https://arxiv.org/abs/2011.08785).
*   **Dataset:** [MVTec AD - Anomaly Detection Dataset](https://www.mvtec.com/company/research/datasets/mvtec-ad)

---

## License

Distributed under the MIT license. See the `LICENSE` file for more details.
