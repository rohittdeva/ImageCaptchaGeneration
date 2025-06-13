# Image CAPTCHA Generation System

This project presents an automated image-based CAPTCHA verification system that uses Convolutional Neural Networks (CNNs) for object classification, image transformation, and a graphical interface via Tkinter.

## 🚀 What It Does
- Uses a CNN to classify object images (e.g., cars, bikes, buses).
- Applies transformations like noise, blur, rotation, and brightness adjustments to simulate CAPTCHA difficulty.
- Generates CAPTCHA challenges where users must select all images of a given object type.
- Features an interactive GUI for user verification.

---

## 🧠 Introduction

CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) helps distinguish between humans and automated bots. While traditional text-based CAPTCHAs are vulnerable to AI-based attacks, image-based CAPTCHAs are more robust. This project explores a smarter solution using deep learning.

---

## ❓ Problem Definition

Text CAPTCHAs can be bypassed by advanced OCR techniques. Hence, there's a need for a system where users verify themselves by selecting images of specific objects, which is more intuitive for humans and harder for bots.

---

## ✅ Solution

This system:
- Trains a CNN model to classify objects like cars, bikes, etc.
- Randomly distorts these images using various augmentation techniques.
- Presents a grid of images and prompts users to select those matching a specified object class.
- Validates user selections using CNN predictions.

---

## 🧱 System Design & Architecture

### 1. Data Collection
- A folder-based dataset organized by object classes (e.g., \`dataset/car\`, \`dataset/bike\`, etc.).
- Data is split into training and validation sets using TensorFlow’s \`ImageDataGenerator\`.

### 2. Model Architecture
- A CNN built with TensorFlow/Keras, using Conv2D, MaxPooling2D, Dropout, and Dense layers.
- Trained using categorical cross-entropy loss and the Adam optimizer.

### 3. Image Preprocessing & Transformation
- Images are resized, normalized, and transformed using:
  - Noise addition
  - Gaussian blur
  - Brightness and contrast adjustment
  - Rotation

### 4. CAPTCHA Generation
- CAPTCHA challenges are auto-generated using random images and transformations.
- A grid layout is created where the user selects images of a prompted object.

### 5. User Interaction
- GUI built with Tkinter.
- Displays the CAPTCHA grid and tracks user selections.
- Provides feedback for correct/incorrect selections and advances levels accordingly.

---

## 📁 Project Structure

\`\`\`
ImageCaptchaGeneration/
├── dataset/                 # Images organized by class
├── captcha_gui.ipynb        # Jupyter Notebook (main logic)
├── model.h5                 # Trained CNN model
├── utils.py                 # Helper functions for transformations and logic
├── requirements.txt         # Python package dependencies
├── README.md                # Project documentation (this file)
\`\`\`

---

## 🧠 Technologies Used
- Python
- TensorFlow / Keras
- OpenCV & Pillow (for image processing)
- Tkinter (for GUI)
- NumPy

---

## ⚙️ How to Run

1. **Install dependencies:**
\`\`\`bash
pip install -r requirements.txt
\`\`\`

2. **Run the notebook:**
\`\`\`bash
jupyter notebook captcha_gui.ipynb
\`\`\`

3. **Follow the GUI prompts** to complete the CAPTCHA challenges.

---

## 🗃️ Dataset Info

Images are stored in the \`dataset/\` directory, with each class in a subdirectory:
\`\`\`
dataset/
├── cars/
├── bikes/
├── bus/
├── train/
\`\`\`

You can add more categories by placing labeled images into new subdirectories.

---

## 📌 Key Features
- Object classification with deep learning (CNN).
- Realistic CAPTCHA with augmented image distortions.
- GUI-based user interaction and feedback.
- Extendable to more object classes easily.

---

## 📬 Future Improvements
- Build a web version using Flask or Streamlit.
- Add session management and user tracking.
- Improve CAPTCHA UX and GUI visuals.
- Include accessibility features for vision-impaired users.

---

## 📄 License

This project is open-source and free to use under the **MIT License**.
