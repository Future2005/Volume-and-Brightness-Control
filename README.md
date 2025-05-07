# Gesture-Based Volume and Brightness Control System

This project allows users to control their system's volume and screen brightness using hand gestures detected through their webcam. By leveraging computer vision and MediaPipe's hand tracking, the system measures the distance between fingers to dynamically adjust system settings — providing a touchless, intuitive way to interact with your device.

Key Features:

* Volume Control: Control the system’s volume using your right hand by changing the distance between your thumb and index finger.
* Brightness Control: Control the screen brightness with your left hand using the same gesture mechanism.
* Real-Time Gesture Recognition: Uses MediaPipe to track hand landmarks in real time and detect gestures based on fingertip distance.
* Visual Feedback: Displays circles and lines between finger tips and shows the camera feed with hand landmark annotations.
* Responsive and smooth controls without the need for external hardware.

Technologies Used:

* Python
* OpenCV
* MediaPipe
* screen-brightness-control
* pycaw (for system volume)
* NumPy
* math.hypot (for distance calculation)

How It Works:

1. The webcam captures live video frames.
2. MediaPipe detects the user’s hands and identifies key finger landmarks.
3. The system tracks the thumb and index finger of each hand.
4. It calculates the distance between those fingers.
5. That distance is mapped (using interpolation) to either brightness level (left hand) or system volume (right hand).
6. pycaw and screen-brightness-control are used to apply the changes to the system in real time.

Requirements:

Install the necessary libraries using pip:

pip install opencv-python mediapipe numpy screen-brightness-control pycaw comtypes

How to Run:

1. Make sure your webcam is enabled.
2. Run the Python script:

python volume\_brightness\_control.py

3. Use your left hand to change brightness, and your right hand to change volume.
4. Press 'q' to exit the program.

Notes:

* The camera feed is mirrored to behave like a mirror — your left hand appears on the right side of the screen.
* Ensure proper lighting so the hand landmarks are detected accurately.
* The system supports up to two hands simultaneously for dual control.

This project provides a simple, hands-free way to manage essential system functions using intuitive gestures — ideal for accessibility, presentations, or touchless environments.
