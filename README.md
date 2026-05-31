# License Plate Recognition using EasyOCR and OpenCV

A simple computer vision project for detecting and recognizing text from vehicle license plate images using **EasyOCR** and **OpenCV**. The notebook also includes a utility to extract frames from a video, which can be useful for license plate recognition from recorded traffic or vehicle footage.

## Project Overview

This repository demonstrates a basic Automatic Number Plate Recognition (ANPR) pipeline using a Jupyter/Google Colab notebook.

The notebook performs the following steps:

1. Install and import required libraries.
2. Load an input vehicle/license plate image.
3. Apply EasyOCR for text detection and recognition.
4. Draw a bounding box around the detected text region.
5. Display the recognized plate text on the image.
6. Extract frames from a video file for further image-based processing.

## Features

- License plate text recognition using EasyOCR
- Image processing using OpenCV
- Bounding box visualization around detected text
- Recognized text overlay on the image
- Video-to-frame extraction utility
- Easy to run in Google Colab or local Jupyter Notebook

## Repository Structure

```text
License-Plate-Recognition/
│
├── platerecognize.ipynb      # Main notebook
├── README.md                 # Project documentation
├── images/                   # Input/output images
│   ├── sample_plate.jpg
│   └── output_result.jpg
└── data/                     # Extracted video frames
```

## Requirements

Install the required Python libraries:

```bash
pip install easyocr opencv-python matplotlib numpy
```

The notebook uses:

```python
easyocr
opencv-python
matplotlib
numpy
os
```

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/License-Plate-Recognition.git
cd License-Plate-Recognition
```

### 2. Open the Notebook

You can run the notebook in:

- Google Colab
- Jupyter Notebook
- VS Code with Jupyter extension

```bash
jupyter notebook platerecognize.ipynb
```

### 3. Set the Input Image Path

In the notebook, update the image path:

```python
IMAGE_PATH = "/content/k.jpg"
```

For local execution, use:

```python
IMAGE_PATH = "images/sample_plate.jpg"
```

### 4. Run EasyOCR

```python
reader = easyocr.Reader(['en'])
result = reader.readtext(IMAGE_PATH)
```

### 5. Visualize the Result

The notebook draws a green bounding box around the detected license plate text and displays the recognized text on the image.


## Applications

- Automatic Number Plate Recognition (ANPR)
- Traffic monitoring
- Parking management systems
- Vehicle entry/exit logging
- Smart surveillance systems



