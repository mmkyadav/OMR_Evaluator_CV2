OMR Sheet Evaluator using OpenCV
This project implements an Optical Mark Recognition (OMR) Sheet Evaluator using Python and OpenCV.
The system automatically evaluates a scanned OMR answer sheet by detecting filled bubbles, comparing them with a predefined answer key, and visually marking correct and incorrect responses.

The project demonstrates core computer vision concepts such as image preprocessing, contour detection, pixel density analysis, and result visualization.

🎯 Objectives

To automatically evaluate OMR answer sheets

To detect filled answer bubbles accurately

To compare detected responses with an answer key

To visually mark:

🟢 Correct answers in green

🔴 Incorrect answers in red

To count correct, incorrect, and unanswered questions

🛠️ Technologies Used

Python

OpenCV

NumPy

📂 Project Workflow

Image Preprocessing

Convert image to grayscale

Apply Gaussian blur to reduce noise

Apply binary thresholding for clear bubble detection

Bubble Detection

Detect contours using OpenCV

Filter contours based on:

Size

Aspect ratio

Area (to remove alignment markers)

Answer Evaluation

Group bubbles per question

Use pixel density analysis to find the filled bubble

Compare detected answer with the answer key

Result Visualization

Draw a green circle around correct answers

Draw a red circle around incorrect answers

Result Summary

Display total correct, incorrect, and unanswered counts

🧠 Key Concept Used

Unlike OCR-based approaches, this project uses pixel density–based OMR evaluation, which is more suitable for detecting filled bubbles in answer sheets.

▶️ How to Run the Project

Clone or download the project files

Install dependencies:

pip install opencv-python numpy


Place a scanned OMR sheet image in your system

Update the image path and answer key in the code:

image_path = r"PATH_TO_OMR_IMAGE"
answer_key = [0, 1, 2, 3, ...]  # A=0, B=1, C=2, D=3


Run the Python script

The evaluated OMR sheet will be displayed with color markings

📊 Output Description

🟢 Green Circle → Correct Answer

🔴 Red Circle → Incorrect Answer

Console output displays:

Correct: X
Incorrect: Y
Unanswered: Z

⚠️ Limitations

Designed for fixed-layout OMR sheets

Assumes 4 options per question (A–D)

Bubble size and spacing must be reasonably consistent

Threshold values may need tuning for different sheets

🚀 Future Enhancements

Support for variable number of options

Automatic answer key detection

Percentage score overlay on image

Export evaluated result as image or PDF

GUI-based file selection

🎓 Academic Note

This project is intended for educational and academic demonstration of OMR evaluation using computer vision techniques and is suitable for final-year or mini-project submissions.

👤 Author

M. Muddu Krishna Yadav
