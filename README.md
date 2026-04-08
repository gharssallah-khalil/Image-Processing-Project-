# Image-Processing-Project-
Building a Panorama for Space Image Dataset
# 🌌 Space Panorama Builder

![Python Version](https://img.shields.io/badge/Python-3.9-blue.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.5-green.svg)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Ubuntu-lightgrey.svg)
![License](https://img.shields.io/badge/License-MIT-orange.svg)

## 📖 Overview
**Space Panorama Builder** is a robust computer vision application designed to construct high-quality, seamless panoramic images from extraterrestrial datasets. Developed as part of a Master's project in Computer Engineering at Beykoz University, this system addresses the unique challenges of space imagery, such as texture-less planetary surfaces, extreme illumination variations, parallax distortion, and limited dataset availability. 

By utilizing a hybrid approach that integrates **SIFT feature detection**, **RANSAC-based homography estimation**, and **multi-band blending with exposure compensation**, this tool successfully overcomes the limitations of traditional stitching methods when applied to lunar and Martian terrains.

## ✨ Key Features
* **Advanced Feature Matching:** Utilizes optimized SIFT algorithms to reliably identify keypoints even on low-contrast, texture-poor planetary surfaces.
* **Robust Alignment:** Employs RANSAC for accurate homography estimation, successfully rejecting outlier matches caused by noisy space data.
* **Seamless Multi-Band Blending:** Integrates exposure compensation and multi-resolution blending to remove visible seams and ghosting artifacts.
* **Interactive GUI:** Built-in Tkinter graphical user interface for intuitive image selection, uploading, and output visualization.
* **High Scientific Fidelity:** Ensures precise topographic alignment, maintaining high Structural Similarity Index (SSIM > 0.9) to preserve geological details.

## 🛠️ Tech Stack & Requirements
* **Language:** Python 3.9
* **Core Libraries:**
  * `OpenCV` (cv2) - Core image stitching and computer vision operations
  * `NumPy` - Efficient matrix and numerical array processing
  * `Matplotlib` / `PIL` - Image handling and visualization
  * `Tkinter` - Graphical User Interface (GUI) framework
* **Hardware Requirements:** Intel Core i7 (or equivalent), 16 GB RAM, NVIDIA GTX 1650 GPU (recommended for large orbital mosaics).

## 📊 Pipeline Architecture
The system follows a modular image processing pipeline designed for reliability and speed:
1. **Image Acquisition & Preprocessing:** GUI-based upload followed by exposure normalization.
2. **Feature Extraction:** Finding correspondences using scale-invariant features.
3. **Geometric Transformation:** RANSAC-driven homography estimation for parallax handling.
4. **Multi-Band Blending:** Seamless integration of overlaps.
5. **Quality Assessment & Panorama Generation:** Outputting high-fidelity stitched visuals.

## 🗂️ Datasets Validated
The system has been rigorously tested and optimized on standardized planetary image archives:
* **LROC NAC:** Lunar Reconnaissance Orbiter Camera (High-resolution Moon surface images).
* **MSL Mastcam:** Mars Science Laboratory (Curiosity rover Martian panoramas).
* **Synthetic Mars Data:** Controlled conditions for baseline benchmarking.

## 🚀 Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/space-panorama-builder.git](https://github.com/yourusername/space-panorama-builder.git)
   cd space-panorama-builder
