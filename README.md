# Human Detect Realtime

Flask web app for human detection in videos and realtime streams.

## Setup

```bash
cd /Users/vigneshswaminathan/human-detect-realtime
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Moondream fallback is optional:

```bash
pip install moondream
```

## Run

```bash
python app.py
```

Open:

```text
http://localhost:5000
```

## Realtime Sources

Use `0` for the computer webcam when OpenCV can access it from the Python process.

You can also use RTSP, HTTP MJPEG, or video stream URLs, for example:

```text
rtsp://user:password@192.168.1.10:554/stream1
http://192.168.1.10/video.mjpg
```

## Model Selection

By default the app loads `yolov8m.pt`. To use a faster model:

```bash
YOLO_MODEL=yolov8n.pt python app.py
```
