# 📄 OMR Sheet Evaluator using OpenCV (Python)

## 📌 Project Overview
This project implements an **Optical Mark Recognition (OMR) Sheet Evaluator** using **Python and OpenCV**.  
The system automatically evaluates a scanned OMR answer sheet by detecting filled bubbles, comparing them with a predefined answer key, and visually marking correct and incorrect responses.

The project demonstrates core **computer vision concepts** such as image preprocessing, contour detection, pixel density analysis, and result visualization.

---

## 🎯 Objectives
- Automatically evaluate OMR answer sheets  
- Detect filled answer bubbles accurately  
- Compare detected responses with an answer key  
- Visually mark:
  - 🟢 Correct answers in **green**
  - 🔴 Incorrect answers in **red**
- Count correct, incorrect, and unanswered questions  

---

## 🛠️ Technologies Used
- Python  
- OpenCV  
- NumPy  

---

## 📂 Project Workflow

1. **Image Preprocessing**
   - Convert image to grayscale  
   - Apply Gaussian blur to reduce noise  
   - Apply binary thresholding for clear bubble detection  

2. **Bubble Detection**
   - Detect contours using OpenCV  
   - Filter contours based on:
     - Size  
     - Aspect ratio  
     - Area (to remove alignment markers)  

3. **Answer Evaluation**
   - Group bubbles per question  
   - Use **pixel density analysis** to find the filled bubble  
   - Compare detected answer with the answer key  

4. **Result Visualization**
   - Draw a **green circle** around correct answers  
   - Draw a **red circle** around incorrect answers  

5. **Result Summary**
   - Display total correct, incorrect, and unanswered counts  

---

## 🧠 Key Concept Used
Unlike OCR-based approaches, this project uses **pixel density–based OMR evaluation**, which is more suitable for detecting filled bubbles in answer sheets.

---

## ▶️ How to Run the Project

1. Clone or download the project files  
2. Install dependencies:
   ```bash
   pip install opencv-python numpy
