# CV-Project

Drowsy Detection System using Eye Aspect Ratio (EAR) with Shape Predictor

**Introduction:**
The Drowsy Detection System utilizes the Eye Aspect Ratio (EAR) calculation, employing the Shape Predictor from the dlib library to identify facial landmarks. EAR is a reliable metric for determining the openness of eyes, crucial in detecting drowsiness or fatigue in individuals. In OpenCV, the shape_predictor_68_face_landmarks model is commonly used to identify these points.

**Dependencies:**
Ensure you have the following dependencies installed:
- Python (>=3.6)
- dlib
- OpenCV
- NumPy

**Getting Started:**
1. Install dependencies using `pip install -r requirements.txt`.
2. Download the pre-trained shape predictor model (shape_predictor_68_face_landmarks.dat) from the dlib website and place it in the project directory.

**Usage:**
1. Run `main.py` to start the drowsy detection system.
2. The system captures video frames from the webcam using OpenCV.
3. Facial landmarks are detected using the Shape Predictor.
4. EAR is calculated based on the change in eye dimensions during blinking or closure.
5. A predefined threshold is used to determine drowsiness.

**Understanding EAR Calculation:**
- To incorporate changes in the x and y axes when the eye is closed, you can modify the coordinates of the points based on your criteria. For example, if closing the eye increases the length of the x-axis and decreases the length of the y-axis, you would adjust the coordinates accordingly before calculating the EAR.
- EAR is calculated as the ratio of the horizontal distance between the inner and outer eye corners to the vertical distance between the upper and lower eyelids.
- When the eyes are open, EAR approaches a higher value.
- Drowsiness is indicated by a significant drop in EAR when the eyes close.
  


**Integration with Alarms (Fututre Work)**
- Integrate the system with alarms or notifications to alert users when drowsiness is detected.
- Customizable alarm options based on the severity of drowsiness.

**Note:**
- Ensure proper lighting conditions for accurate facial landmark detection.
- Experiment with different video resolutions and frame rates for optimal performance.
- Consider user privacy and data security when deploying the system.


**References:**
- dlib: http://dlib.net/
- Shape Predictor Model: http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
 

