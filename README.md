Pose Correction Video Processor
This Python project processes a video to detect and analyze the angles of specific joints in a person's body using MediaPipe and OpenCV. It then provides recommendations for adjustments if joint angles differ significantly from reference angles, overlaying this information directly onto the video frames.

Features
Pose Detection: Uses MediaPipe to detect and track human poses in each frame of the video.
Angle Calculation: Calculates the angles at the elbows and knees.
Angle Comparison: Compares detected angles with predefined reference angles to determine if they are within acceptable thresholds.
Recommendations Overlay: Displays corrective suggestions on the video if a detected angle exceeds the specified threshold.
Video Output: Saves a new version of the input video with recommendations displayed as overlays.
Setup
Requirements
To run this project, you need to install the following Python libraries:

OpenCV: For video processing
MediaPipe: For pose estimation
You can install these libraries via pip:

bash
Copy code
pip install opencv-python-headless mediapipe
Files
shoot_bow.avi: Input video file.
processed_video11.mp4: Output video file with overlaid recommendations.
pose_processor.py: Main Python script that processes the video.
Usage
Set the Input Video Path:

Place your video file in the specified location or change the video_path variable in the script to the path of your video file.
Run the Script:

Run the script by executing:
bash
Copy code
python pose_processor.py
Check the Output:

After the script completes, check processed_video11.mp4 to see the recommendations overlaid on the video.
Reference Angles and Thresholds
The script checks angles for:
Left Elbow
Right Elbow
Left Knee
Right Knee
Reference Angles:
Left and Right Elbows: 160°
Left and Right Knees: 170°
Angle Threshold:
15° difference from the reference angle triggers a recommendation.
You can adjust the REFERENCE_ANGLES and ANGLE_THRESHOLD values in the script as needed.

Customizing Recommendations
The recommendations appear on the video if any joint angle deviates from the reference by more than the threshold. Modify the recommendations section if you want to add or adjust feedback.

Example Output
Each frame in the output video shows the user with pose landmarks, angles, and any recommendations for adjustment.

License
This project is licensed under the MIT License.
