# Object Detection and Tracking with YOLOv8 and Deep SORT

This project performs object detection and tracking on a video file using YOLOv8 for detection and Deep SORT for tracking. It generates an output video with bounding boxes, class labels, and tracking IDs.

## Features
- Object detection using YOLOv8 (default: `yolov8n.pt`).
- Object tracking using Deep SORT.
- Saves output video with annotated bounding boxes and tracking IDs.
- Configurable via command-line arguments.

## Requirements
- Python 3.8+
- Dependencies listed in `requirements.txt`

## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download a YOLOv8 model (e.g., `yolov8n.pt`) from [Ultralytics](https://github.com/ultralytics/ultralytics) or let the script download it automatically.

## Usage
Run the script with a video file:
```bash
python object_detection_tracking.py --video path/to/Test Video.mp4 --output output.mp4 --model yolov8n.pt --conf 0.5
```
- `--video`: Path to input video (e.g., `Test Video.mp4`).
- `--output`: Path to output video (default: `output.mp4`).
- `--model`: YOLOv8 model (default: `yolov8n.pt`).
- `--conf`: Confidence threshold (default: 0.5).

## Example
```bash
python object_detection_tracking.py --video Test Video.mp4
```
This processes `Test Video.mp4` and saves the result to `output.mp4`.

## Notes
- Use a GPU for faster processing.
- Ensure the input video is in a supported format (e.g., MP4, AVI).
- Adjust `--conf` or Deep SORT parameters (`max_age`, `n_init`) for better tracking.

## License
MIT License
