# Doctor‑Strange‑Lite

A lightweight Python/OpenCV demo that overlays "magic circle" effects around detected hands — inspired by the Doctor Strange style. Useful as a fun AR filter or a vision demo.

## ⚙️ Recommended Python version

**Python 3.10 (recommended).**

The project should also work with **Python 3.9 — 3.11**, but using Python 3.10 ensures best compatibility with the tested dependency versions.

## 🔧 Requirements

* Python 3.10 (or 3.9–3.11)
* `pip` (Python package manager)
* A webcam (for real-time demo) or a test video/image

Project dependencies are listed in `requirements.txt`.

## 🚀 Quick start

1. Clone the repository

```bash
git clone https://github.com/vush-man/Doctor-Strange-Lite.git
cd Doctor-Strange-Lite
```

2. (Optional but recommended) Create and activate a virtual environment

```bash
python -m venv .venv
# Linux / macOS
source .venv/bin/activate
# Windows (PowerShell)
.\.venv\Scripts\Activate.ps1
```

3. Install dependencies

```bash
pip install -r requirements.txt
```

4. Run the demo

```bash
python main.py
```

* The script will attempt to open your default webcam (`cv2.VideoCapture(0)`).
* Press `q` in the window to quit the demo.

## 🗂 Project structure

```
Doctor-Strange-Lite/
├── assets/                # magic circle images or overlays
├── main.py                # entry point (hand detection + overlay)
├── requirements.txt       # Python dependencies
├── README.md              # this file
└── hand_landmarks.png     # reference image used by demo
```

## 📝 What it does

* Detects hands (simple landmark/reference-based or OpenCV contours depending on implementation).
* Overlays a stylized circular "magic" graphic centered around detected hand landmarks.
* Lightweight and easy to expand (gesture triggers, sound, more effects).

## ✅ Suggested improvements (if you want to expand)

* Replace or augment basic detection with **MediaPipe Hands** for better multi-finger landmarks and gesture recognition.
* Add gesture-based triggers (e.g., pinch → spawn effect).
* Modularize code: split `main.py` into `hand_detector.py` and `overlay.py`.
* Add tests and an example recorded video to `assets/` for users without a webcam.

## 🛠 Troubleshooting

* **Camera not opening**: Make sure no other app is using the webcam. Try changing the index in `cv2.VideoCapture(0)` to `1` or `2`.
* **Dependency errors**: Recreate the virtual environment and reinstall using `pip install -r requirements.txt`.
* **Low FPS / lag**: Reduce resolution (e.g., `cap.set(cv2.CAP_PROP_FRAME_WIDTH, 640)`), or optimize overlay drawing.

## 📬 Credits

Created by **vush-man**. Inspired by visual effects from Doctor Strange (this project is purely fan-made and for educational/demo purposes only).
