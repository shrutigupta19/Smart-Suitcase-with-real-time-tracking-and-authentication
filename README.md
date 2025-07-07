# Smart-Suitcase-with-real-time-tracking-and-authentication
Step 1: System Initialization
The Raspberry Pi boots up, showing the Raspberry Pi OS desktop interface.
The system checks the camera connection and initializes necessary libraries (e.g., OpenCV).
If GPU or performance issues occur (like horizontal distortion), HDMI cable checks and GPU memory allocation adjustments may be required.

Step 2: Color Calibration & Detection
The Python script Ball_chasing_robot.py is executed from the Freebot directory.
The camera starts capturing live video feed (1920x1080 resolution as configured).
The system uses HSV (Hue, Saturation, Value) color space to filter the specific target color.

Step 3: Real-Time Tracking
Once the color is detected in the frame, a bounding box (usually red) and trajectory lines (green) are drawn to indicate the object's position and movement.
Tracking parameters like hue and speed thresholds can be adjusted using GUI sliders for fine-tuning.

Step 4: Object Chasing Logic (Robot Movement)
The bounding box coordinates are used to determine the object’s direction.
Based on the object’s position (left, center, or right), motor signals are sent to follow or chase the object.
This ensures the robot/suitcase moves dynamically and accurately follows the detected object.

Step 5: Continuous Monitoring and Adjustment
The process runs in a loop to enable spontaneous, real-time tracking.
Feedback from the camera and object position is continuously analyzed for better path prediction.
If the object moves out of frame, the system scans again to reacquire it.

