Automatic Number Plate Recognition

What is Automatic Number Plate Recognition (ANPR)?
In today’s world, ANPR is a common task in computer vision. It means using a computer to find and read car number plates from images or videos.

Where is it used?
Toll collection at highways
Detecting stolen cars
Watching traffic on roads
Smart parking systems

What Are We Building?
We’re creating a basic number plate reader using Python, OpenCV, and EasyOCR. First, we’ll detect the number plate in an image using OpenCV. Then, we’ll extract the number using EasyOCR.

What is OpenCV?
OpenCV is a free tool for working with images and videos. It’s written in C/C++ but can be used in Python. You can do things like:
Detect objects
Edit images
Track motion
It has thousands of built-in functions to help with image processing.

What is EasyOCR?
EasyOCR is a Python library used to read text from images or PDFs. It's useful when you want to detect and extract text automatically. We’ll use it to read the vehicle number from the plate.

How Will We Detect Number Plates?
We’ll use something called a Haar Cascade Classifier. It’s a smart tool trained to detect specific objects — in our case, number plates. It looks for patterns and shapes in the image to find what it’s looking for.
To work well, Haar Cascades need many images of number plates (positive images) and many images without number plates (negative images) during training. For our project, we’ll use a pre-trained model that already knows how to detect number plates.

Requirements
Python 3.x
OpenCV (version 4.5)
EasyOCR (version 1.4)

Steps to Build the Project
Step 1 – Import Packages and Load the Classifier
Import OpenCV and EasyOCR
Load an image using cv2.imread()
Convert the image to grayscale
Load the Haar Cascade file using cv2.CascadeClassifier()
Step 2 – Detect the Number Plate
Use detector.detectMultiScale() to find the plate in the image
Draw a rectangle around the number plate with cv2.rectangle()
Crop the number plate part from the image
Step 3 – Read the Text on the Plate
Create an EasyOCR reader object
Use reader.readtext() to read text from the cropped plate
Use cv2.putText() to display the text on the image

Output Example
The program might print something like:
Detected Text: H~NHZODV2366

Summary
In this project, you learned how to:
Detect objects using Haar Cascades
Read text from images using OCR
Process images using OpenCV
This is the foundation of an automatic number plate recognition system!
