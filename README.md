# Computer-Vision-Face-Detection

## Analysis of Face Recognition Computer Vision Project

This project focuses on implementing a face recognition system using OpenCV in Python. This projects employs Haar-Cascade classifiers to detect faces, eyes, and smiles in both live webcam feeds and static images. Below is a step-by-step breakdown, key methodologies, results, and recommendations. Haar-Cascade Classifiers is a machine learning-based object detection using edge and line features and efficient for real-time applications.

### Methodology

**1.  Setup & Dependencies**
-  Installs opencv-python and imports cv2 for computer vision operations.
-  Utilizes pre-trained Haar-Cascade classifiers for face, eye, and smile detection.

**2.  Haar-Cascade Initialization**

#### Three classifiers were utilised:

-  haarcascade_frontalface_default.xml (face detection).

-  haarcascade_eye.xml (eye detection).

-  haarcascade_smile.xml (smile detection).

**3.  Detection Function (detect)**

-  Converts input frames to grayscale for efficient processing.

-  Face Detection: Uses **detectMultiScale** with a scale factor of **1.3** and minimum neighbors of **5**. Draws a blue bounding box around detected faces.

-  Eye Detection: Scans the face region-of-interest (ROI) with a scale factor of **1.1** and minimum neighbors of **3**. Draws orange bounding boxes around eyes.

-  Smile Detection: Scans the entire grayscale frame (not the face ROI) with a scale factor of **1.2** and minimum neighbors of **10**. Draws green bounding boxes around smiles.

**4.  Real-Time Webcam Implementation**

-  Captures video from the default webcam (**cv2.VideoCapture(0)**, where **0** denotes the default system camera..

-  Processes each frame with the detect function and displays results until the user presses q.

**5.  Static Image Processing**

-  Loads an image from a specified path (e.g Ronaldo.jpg) - _this was used in the project_.

-  Applies the same detection pipeline and displays the annotated image.

### Results

The project demonstrates robust face, eye, and smile detection using OpenCV. It showcases the **potential for applications in;**
-  Security systems (face recognition)
-  User experience analysis(smile detection for feedback)
-  Interactive gaming(eye-tracking)
-  human-computer interaction and facial expression analysis.

### Conclusion

The face recognition project is a solid foundation for more advanced computer vision applications. The use of OpenCV’s Haar-Cascade classifiers provides an accessible and efficient solution for feature detection, making it a valuable addition to a professional data science and computer vision portfolio.
