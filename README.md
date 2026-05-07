# 🏙️ Urban Object Detection AI

A Streamlit-based web application for real-time object detection in urban environments using a custom-trained YOLOv8 model. Upload images or videos and get instant bounding box predictions with class labels and confidence scores.

---

## 📸 Demo

> Upload an image or video → model runs inference → view annotated output directly in the browser.

---

## 🚀 Features

- 📷 **Image detection** — supports `.jpg`, `.jpeg`, `.png`, `.bmp`
- 🎥 **Video detection** — supports `.mp4`, `.avi`, `.mov`, `.mkv`
- 🏷️ **Bounding boxes** with class labels and confidence scores
- ⚡ **YOLOv8-powered** inference via [Ultralytics](https://github.com/ultralytics/ultralytics)
- 🖥️ **Simple browser UI** built with Streamlit — no coding required to use

---

## 🗂️ Project Structure

```
.
├── app.py                  # Main Streamlit application
├── yolov8_model.pt         # Your trained YOLOv8 model weights (not included)
├── temp/                   # Auto-created folder for uploaded & output files
├── requirements.txt        # Python dependencies
└── README.md
```

---

## 🛠️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/urban-object-detection.git
cd urban-object-detection
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 📦 Requirements

Create a `requirements.txt` with the following:

```
streamlit
opencv-python
numpy
ultralytics
Pillow
```

Or install manually:

```bash
pip install streamlit opencv-python numpy ultralytics Pillow
```

---

## ⚙️ Configuration

In `app.py`, update the model path to point to your trained YOLOv8 weights:

```python
model = YOLO('path/to/your/model.pt')
```

> The current path is set to a local Windows path (`G:\mlOps\objectDetection\yolov8 model 2.pt`). Update this before running.

---

## ▶️ Usage

```bash
streamlit run app.py
```

Then open your browser at `http://localhost:8501`, upload an image or video, and the app will display the annotated output.

---

## 🧠 Model

This app uses a **custom-trained YOLOv8** model fine-tuned for urban object detection. The model weights (`.pt` file) are not included in this repository due to file size. You can:

- Train your own model using [Ultralytics YOLOv8](https://docs.ultralytics.com/)
- Or replace the model path with any compatible YOLOv8 `.pt` file

---

## 📋 How It Works

1. User uploads an image or video via the Streamlit interface
2. The file is saved temporarily to the `temp/` directory
3. The YOLO model runs inference on each frame (video) or the full image
4. Bounding boxes, class labels, and confidence scores are drawn using OpenCV
5. The annotated result is displayed back in the browser

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is licensed under the [MIT License].

---

## 👤 Author

**Md Sadman**  
Physics undergraduate | ML & Astrophysics researcher  
[GitHub]((https://github.com/jwsadman)) · [LinkedIn]((https://www.linkedin.com/in/md-sadman-z6))
