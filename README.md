# Final Year Research Project

It is my final year project. I develop a system that can detect face from video captured by webcam. The system keeps track of face movement and moves mouse based on head movement. The challenge is to develop a hands-free Human-Computer Interaction (HCI) system that enables amputees and individuals with limited hand mobility to operate computers effectively. The system needs to accurately interpret eye movements and convert them into meaningful cursor actions.

Library Used

cv2: OpenCV library for computer vision. numpy as np: NumPy library for numerical operations. pynput.mouse: pynput library for controlling the mouse. wx: wxPython library for GUI components. time: Python standard library for time-related functions. Initialization: mouse: pynput mouse controller. app: wxPython application. (sx, sy): Screen size. face_cascade: Haar Cascade classifier for face detection. cap: Video capture object (assumed to be the default camera). Variables:

flag: Variable to determine the mouse action (1 for left click, 2 for right click, 3 for double click). oldx, oldy: Previous mouse coordinates. cnt: Counter for tracking mouse movement. Various coordinates for defining rectangles on the screen. Functions:

color_all(), color_left(), color_right(), color_double(): Functions to draw rectangles with different colors for mouse actions. Main Loop:

Continuously captures frames from the camera, flips the frame horizontally, and converts it to grayscale. Detects faces using the Haar Cascade classifier. Draws rectangles and updates the flag based on the detected face's position. Maps face position to mouse position and performs mouse clicks. Displays the result in an OpenCV window. Exiting the Program:

Pressing the 'Esc' key breaks out of the main loop and releases the video capture. Note: Ensure that you have the required libraries installed (cv2, numpy, pynput, wx). Also, you need the Haar Cascade XML file for face detection (here assumed to be 'haarcascade_frontalface_default.xml'). Make sure your camera is accessible and functional.
