# Star and Streak Detection in Space Images using Self-Supervised CNN 🌌

This repository contains the complete pipeline developed for my internship assessment  at **Digantara**. The goal of this project is to detect **stars and streaks** from high-resolution raw space images using a **self-supervised convolutional neural network (CNN)** approach.

The entire workflow is implemented in a single Jupyter notebook:  
📘 `star.ipynb`

---


---

## ⚙️ Pipeline Overview

1. **Image Preprocessing**
   - CLAHE (Contrast Limited Adaptive Histogram Equalization)
   - Intensity-based thresholding for mask generation

2. **Self-Supervised Label Generation**
   - Patch extraction using sliding window
   - Automatic labeling (streak/star/background) based on masks

3. **CNN Training**
   - Lightweight 3-layer convolutional neural network
   - Trained on auto-labeled patches (no manual annotations needed)

4. **Inference**
   - Sliding window inference on test images
   - Visualization: bounding boxes and colored overlays

---

## 🚀 How to Run

### Step 1: Clone the Repo

```bash
git clone https://github.com/yourusername/Detection-and-Classification-of-Space-Objects--Stars-and-Streaks--in-Astronomical-Images.git
cd Detection-and-Classification-of-Space-Objects--Stars-and-Streaks--in-Astronomical-Images
```
### Step 2: Install Required Libraries

```
pip install torch torchvision opencv-python matplotlib numpy scikit-image tqdm

```
## 📥 Input

Add high-resolution raw space images to the images/ directory.

Supported formats: .png, .jpg, .jpeg, .tiff

Recommended resolution: 4418 × 4418

## 📤 Output

Outputs are saved to outputs/ automatically.

For each image:

Binary mask (thresholded CLAHE)

Annotated image with stars and streaks detected

## 📌 Notes

The CNN learns using noisy masks derived from image processing – no manual annotations are required.

Useful for preliminary object detection in satellite surveillance and SSA tasks.

All parameters (patch size, stride, CLAHE clip limit, thresholds) are adjustable in the notebook.



