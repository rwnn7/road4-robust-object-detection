
```markdown
# Robust Object Detection with YOLOv8 (ROAD4)

This project trains a **baseline YOLOv8 object detection model** and improves robustness under **adverse visual conditions** using synthetic data augmentation and fine-tuning.

The dataset is derived from a small subset of **COCO128**, keeping only four classes:
- person
- car
- truck
- traffic light

The goal is to evaluate how well the model performs on **clean images vs adverse conditions**.

---

# Project Structure

```

AI_Assessment/
│
├── robust_yolov8_road4.ipynb
├── README.md
└── requirements.txt

````

- **robust_yolov8_road4.ipynb**  
  Full pipeline including dataset preparation, training, evaluation, and robustness analysis.

- **requirements.txt**  
  Python dependencies required to run the notebook.

- **README.md**  
  Project description and instructions.

---

# Setup

Install dependencies:

```bash
pip install -r requirements.txt
````

---

# How to Run

Open the notebook and run all cells:

```
robust_yolov8_road4.ipynb
```

The notebook will automatically:

1. Load the COCO128 dataset.
2. Create the **ROAD4 clean dataset** containing the selected classes.
3. Generate an **adverse test set** using image degradations such as:

   * brightness and contrast changes
   * gamma shifts
   * noise
   * motion blur
   * JPEG compression
4. Train a **baseline YOLOv8 model**.
5. Fine-tune a **robust model** using augmented training data.
6. Evaluate both models on:

   * clean test data
   * adverse test data.
7. Compare performance using:

   * Precision
   * Recall
   * mAP50
   * mAP50-95

The notebook also generates **plots and comparison tables** showing robustness differences between the models.

---

# Reproducibility

The experiment uses a **fixed random seed** and deterministic settings where possible to reduce run-to-run variation.

---

# Libraries Used

* Ultralytics YOLOv8
* PyTorch
* Albumentations
* NumPy
* Pandas
* OpenCV
* Matplotlib

---

# Notes

The dataset and training outputs are **not stored in the repository**.
They are automatically generated when running the notebook.


