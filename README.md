# R&D: Medical Image Processing with DICOM Data

## 📌 Project Overview

This repository contains a research-oriented notebook focused on the analysis and preprocessing of medical images in DICOM format.
The work explores fundamental steps of medical image processing, including volumetric data construction, metadata analysis, pixel normalization, format conversion, and window-based visualization for different anatomical structures.

The project is designed as an R&D exercise to study low-level image representations used in medical imaging pipelines.

---

## 🎯 Research Goal

To explore and implement core algorithms for medical image preprocessing using real DICOM datasets, with emphasis on understanding pixel intensity representations, metadata structure, and visualization techniques commonly applied in clinical imaging.

---

## 🧪 Research Tasks and Algorithmic Flow

### Task 1: DICOM Volume Construction (Chest CT)

**Algorithmic steps:**

1. Load a series of DICOM slices from a directory
2. Sort slices to preserve anatomical order
3. Stack slices into a 3D NumPy volume
4. Inspect voxel values in Hounsfield Units (HU)
5. Visualize all slices of the reconstructed volume

**Purpose:**
To understand volumetric CT data representation and raw pixel intensity distribution.

---

### Task 2: DICOM Metadata Analysis and Image Conversion (Knee CT)

**Algorithmic steps:**

1. Load DICOM files using `pydicom`
2. Extract and analyze metadata (scanner, acquisition parameters, patient anonymization)
3. Visualize raw DICOM images
4. Normalize pixel values to `[0, 255]`
5. Convert selected slices to PNG format

**Purpose:**
To study DICOM metadata structure and differences between raw medical images and normalized visual formats.

---

### Task 3: Window-Based Image Visualization (Chest CT)

**Algorithmic steps:**

1. Load DICOM slices and extract pixel arrays
2. Apply windowing function using configurable `window_center` and `window_width`
3. Generate specialized visualization modes:

   * **Bone Window** – emphasizes high-density structures
   * **Lung Window** – highlights lung tissue and air regions
4. Normalize and apply optional gamma correction
5. Compare original DICOM images with windowed PNG outputs

**Purpose:**
To demonstrate how clinical visualization relies on window functions to reveal different anatomical features from the same data.

---

## 📥 Input Data

* Chest CT DICOM dataset
* Knee CT DICOM dataset
* Raw pixel data stored in Hounsfield Units
* Full DICOM metadata

---

## 📤 Output Data

* 3D volumetric NumPy arrays
* Metadata inspection outputs
* Normalized PNG images
* Windowed visualizations (Bone / Lung)

---

## 🧠 Technologies and Libraries

* **Programming Language:** Python
* **Medical Imaging:** pydicom
* **Numerical Computing:** NumPy
* **Visualization:** Matplotlib
* **Image I/O:** imageio, PIL
* **Environment:** Google Colab / Jupyter Notebook

---

## 📂 Repository Structure

```
/notebooks
  medical_image_processing_rnd.ipynb   # Main R&D notebook
```

---

## ✅ Research Outcomes

* Reconstructed 3D medical image volumes from DICOM slices
* Explored real clinical metadata and acquisition parameters
* Implemented pixel normalization and format conversion
* Applied window-based visualization for anatomical analysis
* Built a reusable preprocessing pipeline for medical imaging experiments

---

## 🧪 Project Status

Research notebook completed.
The repository serves as a foundational R&D study for further work in medical image analysis, computer vision, and machine learning applied to healthcare.

