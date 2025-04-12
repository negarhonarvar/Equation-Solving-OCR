# Equation Solver with OCR

This repository implements a full pipeline to classify and solve equations from images using deep learning and OCR techniques. It supports both **handwritten** and **typed** expressions and reconstructs them into solvable strings.

## Overview 🚀

The system processes input equation images by:

- Classifying the equation as handwritten or typed
- Segmenting and recognizing characters using:
  - CNN trained on MNIST and a custom symbol dataset
  - Tesseract and EasyOCR for OCR-based recognition
- Reconstructing the equation
- Solving the expression and saving results

## Dataset 📁

All training and test data are available in this shared Google Drive folder:

[Equation Dataset - Google Drive](https://drive.google.com/drive/folders/13nICjIQg57NhPn5eYJwZp1jCpJwk4vjp)

## How to Use 🛠

### 1. Clone the Repository

    git clone https://github.com/yourusername/equation-ocr-solver.git
    cd equation-ocr-solver
    
### 2. Install Dependencies

    pip install -r requirements.txt
    
If you're running in Google Colab, also install Tesseract with:

    !apt-get install tesseract-ocr
    
### 3. Run the Notebook
Open and run the following notebook in Google Colab:

    EquationSolving-OCR.ipynb

### 4. Output
After running the full pipeline, a file named submission.csv will be generated containing:

  - The predicted type of each equation image (typed or handwritten)

  - The evaluated result of the expression

## Project Structure 📦

    ├── README.md
    ├── requirements.txt
    ├── EquationSolving-OCR.ipynb         # Original notebook (Colab)
    ├── equationsolving_ocr.py            # Exported script version of the notebook
    ├── drive/
    │   ├── train/                         # Training images
    │   ├── test/                          # Test images
    │   ├── train_info.csv                 # Labels for training
    │   └── submission.csv                 # Generated predictions

## License 🧾
This project is licensed under the MIT License. See the LICENSE file for details.
