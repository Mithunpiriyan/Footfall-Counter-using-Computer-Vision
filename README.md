# Footfall-Counter-using-Computer-Vision
To develop a computer vision–based system that counts the number of people entering and exiting through a specific area (like a doorway, corridor, or gate) using object detection, tracking, and region-of-interest (ROI) logic.
### Tools and Technologies

* Programming Language: Python 3.8+
* Detection Model: YOLOv8 (Ultralytics)
* Tracking: Centroid-based logic with object IDs
* Visualization: OpenCV
* Execution Environment: Jupyter Notebook or Python Script
  



### Setup Instructions



#### 1.Install Dependencies

Run the following in your terminal or Jupyter Notebook cell:
bash
pip install -r requirements.txt


or manually install:
pip install ultralytics opencv-python numpy matplotlib



#### 2.Download YOLOv8 Model (automatically handled)

#### 
The code uses the YOLOv8 Nano model:
python
model = YOLO("yolov8n.pt")
If the model is not found, it will be downloaded automatically by Ultralytics.


#### 3.Run the Footfall Counter

Using webcam:
python footfall\_counter.py
or open and run each cell in the provided Jupyter Notebook (footfall\_counter.ipynb).

Press 'Q' to quit the live webcam feed.


### Counting Logic
* The system defines a horizontal ROI (counting line) at the center of the frame.
* For every detected person, it calculates the centroid (center of bounding box).
* If a centroid crosses the line from top → bottom, it is counted as Entry.
* If it crosses from bottom → top, it is counted as Exit.
* Entry and Exit counts are displayed dynamically on the video.



### Output
### 
Real-time bounding boxes drawn around detected people.
Entry and Exit counts displayed on the screen.

Example overlay text:

Entered: 5

Exited: 3


