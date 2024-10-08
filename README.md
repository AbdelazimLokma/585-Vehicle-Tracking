# Single and Multi-Object Tracking with Bayesian and Kalman Filters

This project focuses on implementing object tracking algorithms for both single and multiple objects in a video. 
The main goal is to provide a smooth 2D track for detected objects using an Alpha-Beta or Kalman filter for single-object tracking, and to assign 
unique IDs for multiple objects over time using multi-object tracking and data association techniques.

## Project Structure
```
 ├── A3.ipynb # Main notebook implementing tracking algorithms 
 ├── commonwealth.mp4 # Test video file
 ├── frame_dict.json # Bounding box data for frames 
 ├── obj_detections_test.json # Object detections with IDs over multiple frames 
 ├── object_to_track.json # Specific object tracking data 
 ├── part_1_demo_with_kalman.mp4 # Demo of part 1 with Kalman filter 
 ├── part_1_object_tracking.json # Tracking data for part 1 
 ├── part_2_demo.mp4 # Demo of part 2 for multi-object tracking 
 ├── part_2_frame_dict.json # Bounding box data for part 2
```
## Objectives

### 1. **Single Object Tracking**
   - **Goal**: Given detected 2D positions of a vehicle in multiple video frames, smooth the 2D trajectory using an Alpha-Beta or Kalman filter.
   - **Approach**: Implement a recursive Bayesian filter to predict the next location of the object based on past observations. A Kalman filter is commonly used for this type of tracking due to its ability to handle noisy data and generate a smooth track.

### 2. **Multi-Object Tracking and Data Association**
   - **Goal**: Given bounding boxes of multiple objects detected in each frame, track each object over time and assign unique IDs.
   - **Approach**: Use data association methods (e.g., Hungarian algorithm or IoU matching) to maintain consistent object identities across frames, even when objects move or overlap. Trackers are updated using the bounding box coordinates for each object.

## Key Files

- **A3.ipynb**: Jupyter Notebook containing the implementation of both single and multi-object tracking algorithms.
- **commonwealth.mp4**: Input video used for testing tracking algorithms.
- **frame_dict.json**: Contains bounding box coordinates for detected objects in each frame.
- **obj_detections_test.json**: Contains object detection data with bounding boxes and assigned object IDs for testing multi-object tracking.
- **object_to_track.json**: Contains the 2D coordinates of the single object to be tracked.
- **part_1_demo_with_kalman.mp4**: Demonstration video showing the results of single object tracking using the Kalman filter.
- **part_1_object_tracking.json**: JSON file containing the tracking data for part 1 (single object tracking).
- **part_2_demo.mp4**: Demonstration video showing the results of multi-object tracking.
- **part_2_frame_dict.json**: JSON file containing the bounding box data for multi-object tracking.

## How to Run

1. **Install Dependencies**:
   Make sure you have the necessary Python packages installed. You can install them using the following command:

   ```bash
   pip install -r requirements.txt
