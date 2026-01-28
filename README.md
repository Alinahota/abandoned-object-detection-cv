# Detection of Abandoned Objects and Tracking of Owners for Early Warning Systems


## 📌 Overview

This repository contains the **Final project report (thesis)** for the undergraduate major project titled:

> **“Detection of Abandoned Objects, Identification and Tracking of Their Owners for Early Warning of Terror Attacks”**

The project proposes an **intelligent video surveillance pipeline** capable of:
- Detecting **static (abandoned) objects** in public spaces
- **Identifying and tracking the object’s owner**
- Classifying threat levels and raising alerts in real time

The system is designed to be **robust, computationally efficient**, and suitable for deployment on **low-power embedded systems** integrated with existing CCTV infrastructure.

---

## 🧠 Key Contributions

- Real-time **abandoned object detection** using foreground extraction and IOU-based static analysis  
- **Owner identification** via spatial proximity and backtracking  
- **Owner tracking** using Kalman Filters for occlusion-robust tracking  
- **Threat level classification** (attended / unattended / abandoned)  
- Optimized pipeline using **lightweight deep learning models** suitable for embedded deployment  

---

## 🏗️ System Architecture (High Level)

1. **Preprocessing**
   - Grayscale conversion
   - Gaussian blurring for noise reduction

2. **Foreground Extraction**
   - Background subtraction
   - Canny edge detection
   - Morphological operations

3. **Static Object Detection**
   - Intersection-over-Union (IOU)–based temporal consistency check

4. **Static Object Classification**
   - MobileNet-based human vs non-human classification

5. **Owner Identification**
   - Backtracking to identify closest human when object was placed
   - YOLOv3-Tiny for fast human detection

6. **Owner Tracking**
   - Kalman Filter–based tracking across frames

7. **Alert Classification**
   - Attended
   - Unattended
   - Abandoned (alarm raised)

---

## 🛠️ Technology Stack (as per original project)

- **Language:** Python 3  
- **Libraries & Tools:**
  - OpenCV
  - NumPy
  - YOLOv3-Tiny
  - MobileNet
  - Kalman Filters

---

## 📊 Evaluation

The system was evaluated on standard surveillance datasets:
- **ABODA**
- **AVSS 2007**
- **PETS 2006**

Key results:
- High precision and recall across datasets
- Real-time performance (~140 FPS) even on CPU-only systems
- Robustness to illumination changes, occlusions, and crowded scenes

Detailed metrics and comparisons are available in the report.

---


> ⚠️ **Note:**  
> The original source code developed during the project is no longer available.  
> This repository serves as a **research and documentation archive** of the project.

---

## 🔮 Future Work

- Re-implementation using modern object trackers (e.g., YOLOv8 + DeepSORT)
- Integration with edge devices (Jetson Nano, Raspberry Pi)
- Multi-camera owner re-identification
- Real-time alert dashboards

---

## 👩‍💻 Authors

- **Alina Hota**  
- Radhika Berry  
- Sarah Khan  

**Supervisor:** Dr. Kapil Dev Tyagi  
Department of ECE, JIIT Noida

---

## 📜 License

This repository is shared for **academic and research reference purposes only**.  
Please cite the original authors if using this work.


