# Intelligent CAPTCHA Verification System

This project creates an image-based CAPTCHA system using Convolutional Neural Networks (CNNs) and a Tkinter GUI.

## 🚀 What It Does
- Uses a CNN to classify images (e.g., cars, bikes).
- Adds transformations like noise, blur, brightness to images.
- Generates CAPTCHAs where users select all images of a target object.
- Uses a GUI built with Tkinter for interaction.

## 📁 Project Structure
```
ImageCaptchaGeneration/
├── dataset/                 # Images organized by class
├── captcha_gui.ipynb        # Jupyter Notebook (main logic)
├── model.h5                 # Trained CNN model (if available)
├── utils.py                 # Helper functions (optional)
├── README.md                # This file
```

## 🧠 Technologies Used
- Python
- TensorFlow / Keras
- OpenCV / Pillow (image processing)
- Tkinter (GUI)
- NumPy

## ⚙️ How to Run
1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the notebook:
```bash
jupyter notebook captcha_gui.ipynb
```

OR if it's a `.py` file:
```bash
python captcha_gui.py
```

## 🗃️ Dataset Info
Images are stored in `dataset/` folder. Each class has its own subfolder:
```
dataset/
├── cars/
├── bikes/
├── ...
```

## 🎯 Goal
Make CAPTCHA harder for bots but easy for humans, using AI.

## 📌 Features
- Object recognition with CNN
- CAPTCHA image generation with transformations
- GUI with user interaction and feedback

## 📬 Future Improvements
- Web version using Flask or Streamlit
- More object classes
- Better GUI design

## 📄 License
This project is open-source and free to use under the MIT License.