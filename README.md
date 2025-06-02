# Depth Estimation Using OpenCV

A Python project for **real-time depth estimation** using stereo vision, leveraging OpenCV and live video from two cameras. This system demonstrates the practical use of computer vision to compute accurate depth and disparity maps — essential for robotics, augmented reality, and autonomous vehicle applications.

---

## Overview

This project implements stereo vision algorithms using Python to produce real-time depth maps from two synchronized cameras. It uses adaptive calibration, image rectification, and disparity computation to deliver robust and accurate depth information.

**Key Features:**
- Real-time video capture from two cameras
- Background removal for cleaner stereo matching
- Image preprocessing and rectification
- Stereo Semi-Global Block Matching (SGBM) for disparity and depth calculation
- Visualization of disparity and depth maps
- Average depth and disparity statistics printed to console

---

## Demo

> **Note:** The code is designed for use with two connected cameras (e.g., Logitech webcams) and the `SelfiSegmentation` module from `cvzone`.

---

## Requirements

- Python 3.7+
- OpenCV (`opencv-python`)
- numpy
- cvzone
- (Optional) Jupyter Notebook for experimentation

Install all dependencies with:
```bash
pip install opencv-python numpy cvzone
```

---

## Usage

1. **Connect two cameras** to your computer.
2. **Clone this repository** and navigate to the project directory.
3. **Run the script:**  
   ```bash
   python stereo_vision_group5.py
   # or use the .ipynb notebook in Google Colab or Jupyter
   ```
4. **Press 'q'** to exit the live display.

---

## How it Works

1. **Camera Setup:**
   - Captures video frames from two different cameras (ensure you use the correct device indices).
   - Sets the frame size and FPS.

2. **Background Removal:**
   - Uses `cvzone.SelfiSegmentation` to remove the background for both frames, improving stereo matching.

3. **Preprocessing:**
   - Converts images to grayscale and applies smoothing.

4. **Stereo Matching:**
   - Uses OpenCV’s StereoSGBM algorithm to compute disparity and depth maps.

5. **Visualization:**
   - Displays both the grayscale disparity map and the colorized depth map in real time.

6. **Statistics:**
   - Prints average disparity and average depth values to the console.

---

## Methodology

- **Stereo Vision Algorithm:** Real-time depth estimation using synchronized stereo images.
- **Adaptive Calibration:** Each camera is calibrated to account for unique traits and variances.
- **Image Rectification:** Corrects lens distortion for accurate stereo matching.
- **Disparity Computation:** Computes depth from the stereo pairs using SGBM.
- **Accuracy Assessment:** Evaluates the accuracy and precision of the system for practical use.

---

## Applications

- Robotics navigation
- Augmented reality
- Autonomous vehicles
- 3D scene reconstruction

---

## References

- [OpenCV Documentation: Stereo Vision](https://docs.opencv.org/master/d9/d0c/group__calib3d.html)
- [cvzone SelfiSegmentation](https://github.com/cvzone/cvzone)

---

## License

MIT License

---

**Author:** [sadhanasharma26](https://github.com/sadhanasharma26)
