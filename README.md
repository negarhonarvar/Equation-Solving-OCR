# Equation Solver with OCR
This repository implements a complete pipeline for classifying and solving equations using OCR from image data. The system detects whether an equation is handwritten or typed, segments and classifies individual characters, reconstructs the expression, and evaluates the result.

## Overview
The pipeline processes images containing mathematical equations, determines their type, recognizes characters using CNNs and OCR (Tesseract + EasyOCR), reconstructs expressions, and computes their numeric value.

## Typed/Handwritten Classification using ResNet18

Character Recognition via two methods:

 - CNN trained on MNIST + custom symbol dataset

 - Tesseract/EasyOCR for robust character detection

 - Expression Evaluation using standard parsing and heuristics

 - Output as CSV submission with predicted type and solved value

Dataset
The dataset used in this project (train/test images and labels) is available publicly on Google Drive:

📂 Access Dataset Here

How to Use 📋
Clone the Repository:

bash
Copy
Edit
git clone https://github.com/yourusername/equation-ocr-solver.git
Install Dependencies: Required packages include torch, torchvision, pytesseract, opencv-python, easyocr, Pillow, and others.

bash
Copy
Edit
pip install -r requirements.txt
Run on Google Colab: Open and execute the original notebook: EquationSolving-OCR.ipynb

Output: A submission.csv file will be generated with classification (typed/handwritten) and evaluated result.

Project Structure
bash
Copy
Edit
├── README.md
├── requirements.txt
├── EquationSolving-OCR.ipynb      # Original Colab notebook
├── equationsolving_ocr.py         # Exported .py version of the notebook
├── drive/                         # Google Drive folder (public dataset)
│   ├── train/                     # Training images
│   ├── test/                      # Test images
│   ├── train_info.csv             # Labels for training set
│   └── submission.csv             # Output predictions
License 🛡️
This project is licensed under the MIT License. See the LICENSE file for more details.
