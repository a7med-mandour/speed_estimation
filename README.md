# 🚗 Speed Detection in Video using YOLOv8, Object Tracking, and Perspective Transformation

This project demonstrates a **speed detection system** that processes video footage to detect, track, and calculate the speed of vehicles using **YOLOv8**, **ByteTrack object tracking**, and **perspective transformation**.

## 🚀 Features

- **YOLOv8 Object Detection**: Detect vehicles in each frame with high accuracy.
- **ByteTrack Object Tracking**: Track objects across multiple frames to maintain consistent identification.
- **Perspective Transformation**: Correct perspective distortion in the video to calculate accurate distances.
- **Speed Calculation**: Compute the speed of each tracked vehicle in km/h using moving average distance and time.
- **Video Annotation**: Annotate each frame with vehicle bounding boxes, labels (ID and speed), and trace paths.

## 🛠️ Technologies Used

- **YOLOv8**: For object detection in video frames.
- **OpenCV**: For perspective transformation and video processing.
- **ByteTrack**: For object tracking across frames.
- **Supervision**: For video frame annotation and utility functions.
- **NumPy**: For mathematical operations.


## ⚙️ Code Explanation

The main components of the project are as follows:

1. **PerspectiveTransformer Class**: 
   - Corrects the perspective distortion for accurate distance calculation between frames.

2. **YOLOv8 Object Detection**:
   - Detects vehicles in each frame of the video using the `yolov8n.pt` model.

3. **Object Tracking with ByteTrack**:
   - Ensures that each detected vehicle is consistently tracked across frames.

4. **Speed Calculation**:
   - The speed of each vehicle is computed in km/h based on moving average distance and frame rate.

5. **Video Annotation**:
   - Bounding boxes, labels (showing vehicle ID and speed), and trace paths are drawn on the video frames.

## 🔍 Key Functions

- `get_video_frames_generator()`: Extracts frames from the video for processing.
- `perspectiveTransform()`: Corrects for camera perspective to calculate real-world distance.
- `calculate_optimal_line_thickness()`, `calculate_optimal_text_scale()`: Functions to scale the annotation thickness and size.
- `ByteTrack()`: Tracks object movements and updates vehicle positions.
- `speed = dist / time * 3.6`: Formula used to calculate vehicle speed in km/h.

## 📈 Output

Each frame of the video is processed, and an annotated version is saved:
- **Bounding Boxes**: Show the detected vehicle positions.
- **Labels**: Display vehicle IDs and their calculated speed.
- **Trace Paths**: Indicate the movement path of the tracked vehicles.

## 📝 Future Improvements

- Enhance the accuracy of speed calculation with more advanced calibration methods.
- Extend the system to support additional object categories (e.g., pedestrians, cyclists).
- Implement real-time processing using live video feeds.

## 🎥 Sample Video

You can see the annotated output in the file `out.mp4` after running the script.

---

Feel free to reach out if you have any questions or feedback!

# Tags
`#ComputerVision` `#YOLOv8` `#DeepLearning` `#ObjectDetection` `#AI` `#OpenCV` `#VideoProcessing` `#SpeedDetection`
