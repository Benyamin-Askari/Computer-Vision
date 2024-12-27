Vehicle Counting Using YOLO and ByteTrack

This project is one of the assignments for the IoT priciples modules. it implements vehicle detection, tracking, and counting using the YOLO model combined with ByteTrack. The annotated output video highlights identified vehicles (cars and trucks), tracks their movements, and counts them based on their direction of travel. The complete pipeline includes installing necessary packages, initializing the model, processing video frames, and generating an annotated output video.

Workflow Overview

1. Install Necessary Packages

ultralytics: For YOLO model implementation.

opencv-python: For video processing and frame manipulation.

ffmpeg-python: For handling video input/output formats.

2. Importing Libraries and Initializing the Model

YOLO Model Initialization:

The YOLO model is loaded using a custom weight file (yolo11x.pt).

Class IDs and names are verified to filter relevant classes (e.g., cars and trucks).

3. Set Input and Output Video Paths

Input video is specified for processing.

Output video path is defined for saving the annotated results.

4. Initialize Video Capture and Writer

Captures input video properties (e.g., frame size, FPS).

Configures a video writer for saving the annotated video using the MP4 format.

5. Initialize Counters and Tracking Structures

Sets up counters for tracking vehicles based on type (car, truck) and direction (in, out).

Initializes tracking structures to monitor vehicle positions and ensure accurate counts.

6. Define Helper Functions

Drawing Counting Line: Marks a reference line on the video to track vehicle crossings.

Direction Determination: Identifies whether a vehicle moves "in" or "out" relative to the counting line.

Class Filtering: Filters detections to include only desired vehicle classes (car and truck).

7. Processing Video Frames

Detection and Tracking:

Each frame is processed using YOLO and ByteTrack for detection and tracking.

Bounding boxes, class IDs, and unique track IDs are extracted for each detected object.

Count Updates:

Counts are updated based on vehicle type and direction of travel when crossing the line.

Frame Annotation:

Annotates frames with bounding boxes, labels, and vehicle counts.

Output Video:

The annotated frames are saved to the output video file.

8. Create Download Link for Output Video

Generates a download link for retrieving the annotated video in environments like Google Colab.

Key Features

Vehicle Detection: Uses YOLO for accurate real-time object detection.

Tracking: ByteTrack ensures consistency in tracking individual vehicles across frames.

Counting: Maintains separate counters for cars and trucks moving "in" or "out."

Annotation: Provides clear visualization with bounding boxes, labels, and count overlays.

Applications

This pipeline is suitable for:

Traffic analysis.

Vehicle monitoring systems.

Automated traffic flow optimization.

Output

The annotated video includes:

Vehicles marked with bounding boxes and unique IDs.

Real-time counts of cars and trucks moving in both directions.

With this robust pipeline, vehicle detection and tracking are streamlined, offering an efficient solution for computer vision-based traffic monitoring tasks.

