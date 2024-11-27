# OMR-SHEET-RECOGNIZER
It is a simple OMR Sheet analyzer
Simple Python OMR Recognition Project
This project uses Python for Optical Mark Recognition (OMR) to automatically detect and process marked answers on OMR sheets. The system identifies filled circles on scanned images of OMR sheets and processes them to extract the selected answers.

Features
Detects filled bubbles on an OMR sheet.
Processes scanned images (JPEG, PNG, or PDF) to extract answers.
Can be customized for different types of OMR sheets.
Supports basic error handling for misalignments or unclear markings.
Installation
Prerequisites
Ensure that you have the following installed:

Python 3.6+
pip (Python package installer)
Install Dependencies
Use pip to install the required libraries:

bash
Copy code
pip install opencv-python numpy imutils
Optional
If you're using PDFs or non-image formats, you might need to install additional libraries:

bash
Copy code
pip install pdf2image
Usage
Prepare OMR Sheet Image: Ensure that the OMR sheet image is clear and well-aligned.

Run the Script: Execute the script with the OMR sheet image as input:

bash
Copy code
python omr_recognition.py input_image.jpg
Processing: The script will process the image, detect the marked bubbles, and output the result.

Output: The detected answers will be displayed on the terminal or saved to a result file, depending on your configuration.

Example Command:
bash
Copy code
python omr_recognition.py sample_omr_sheet.png
This will output the detected answers to the terminal.

File Structure
graphql
Copy code
/OMR-Recognition-Project
    ├── omr_recognition.py          # Main script for OMR recognition
    ├── sample_omr_sheet.png        # Example OMR sheet for testing
    ├── README.md                  # Project documentation
    └── requirements.txt            # List of dependencies
Code Explanation
omr_recognition.py
This is the main Python script that handles the OMR recognition process. It uses OpenCV for image processing and NumPy for array manipulations.

Key Steps in the Code:

Image Preprocessing: The input image is resized, converted to grayscale, and thresholded to identify the bubbles.
Bubble Detection: The script identifies circular contours and matches them with predefined locations.
Answer Extraction: Based on the position of the bubbles, the selected answers are extracted and stored.
Contributing
If you'd like to contribute to this project, feel free to fork the repository and submit pull requests. Make sure to follow the project's code style and structure.
