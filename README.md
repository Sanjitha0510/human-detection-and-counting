# Human Detection and Counting

Real-time human detection and counting using YOLOv4-Tiny with OpenCV DNN. Supports image files, video files, and live webcam input.

## Features
- Detects people in images/video/webcam
- Draws bounding boxes and labels (Person N)
- Displays live status and total count overlay

## Requirements

Install Python 3.8+ and the following packages:

```bash
pip install opencv-python imutils numpy
```

## Model Files (YOLOv4-Tiny)

Download the following files and place them in the project root (same folder as `human_detection.py`):
- `yolov4-tiny.cfg`
- `yolov4-tiny.weights`
- `coco.names` (already included)

You can obtain the cfg/weights from official YOLO resources or mirrors. Ensure the filenames exactly match what the script expects.

## Usage

Run the script with one of the supported input types: `image`, `video`, or `webcam`.

```bash
python human_detection.py --input_type image --input_path /absolute/path/to/your_image.jpg
```

```bash
python human_detection.py --input_type video --input_path /absolute/path/to/your_video.mp4
```

```bash
python human_detection.py --input_type webcam
```

Press `q` to quit in video/webcam modes.

## Notes
- The script uses OpenCV DNN with YOLOv4-Tiny for speed on CPU. For best results, ensure adequate lighting and clear visibility of people.
- Default confidence/NMS thresholds are defined at the top of `human_detection.py` and can be tuned:
  - `MIN_CONFIDENCE = 0.2`
  - `NMS_THRESHOLD = 0.3`
- Outputs for image mode are saved to a local folder defined in the script. Update `output_folder` in `detect_by_input` if needed.

## Repository

GitHub repository: `https://github.com/Sanjitha0510/human-detection-and-counting`

## License

This project is provided as-is for educational purposes. Review and update licensing as appropriate for your use case.